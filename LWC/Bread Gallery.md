Bread Gallery
============================

프로젝트 때 제작한 LWC

</br>

<img src="https://github-production-user-asset-6210df.s3.amazonaws.com/99719661/320201284-786ed1df-fe04-4c11-8b75-5a277e2813d4.jpg?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAVCODYLSA53PQK4ZA%2F20240406%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Date=20240406T113850Z&X-Amz-Expires=300&X-Amz-Signature=36dca0a4521cfc8fa74658ab537ae4e8c12b5be1eca5c3aac38b5b4a44a0a027&X-Amz-SignedHeaders=host&actor_id=99719661&key_id=0&repo_id=750716809" width="300" height="450"/>

</br>

<img src="https://github-production-user-asset-6210df.s3.amazonaws.com/99719661/320201293-91632cf8-959e-4291-b8fb-5d996cf6fe45.jpg?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAVCODYLSA53PQK4ZA%2F20240406%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Date=20240406T114025Z&X-Amz-Expires=300&X-Amz-Signature=45febf2ee421b4bc2c2eb2be0d93dc2c75d06d2101d9444fdc0d9a5ab1384af7&X-Amz-SignedHeaders=host&actor_id=99719661&key_id=0&repo_id=750716809" width="300" height="450">

</br>

## CSS

```CSS

.gallery {
    display: flex;
    flex-wrap: wrap;
    gap: 20px;
    text-align: center;
}

.pictureItem {
    flex-basis: calc(33.333% - 20px);
    display: flex;
    flex-direction: column;
    align-items: center;
}

.pictureItem img {
    width: 100%;
    height: auto;
    border-radius: 8px;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
    transition: transform 0.3s ease-in-out;
}

.pictureItem img:hover {
    transform: scale(1.05);
}

.container-label {
    font-size: 30px;
    font-weight: bold;
    text-align: center;
    margin-bottom: 40px; /* product와의 간격 설정 */
    background-color: #fde2cf;
    background-image: url('bread_pattern.png');
    border: 2px solid #dd9d5e;
    border-radius: 10px;
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
    padding: 10px 20px;
    color: #8b5a33;
}

.title {
    font-size: 16px;
    font-weight: bold;
    margin-top: 20px;
    text-align: center;
}

.modal {
    position: fixed;
    top: 50%;
    left: 50%;
    width: 450px;
    transform: translate(-50%, -50%);
    background-color: #f9f9f9;
    padding: 20px;
    z-index: 9999;
    border-radius: 10px;
    box-shadow: 0 0 40px rgba(0, 0, 0, 0.3);
    max-width: 80%;
}

.modal-content {
    text-align: center;
}

.modal-header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-bottom: 20px;
}

.modal-title {
    font-size: 20px;
    font-weight: bold;
}

.close {
    cursor: pointer;
    font-size: 24px;
}

.modal-body {
    margin-bottom: 20px;
}

.selected-product-image {
    max-width: 100%;
    max-height: 300px;
    border-radius: 8px;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
}

.description {
    font-size: 14px;
    margin-top: 20px;
    text-align: left;
}

.modal-footer {
    text-align: center;
}

.btn-close {
    padding: 10px 20px;
    font-size: 16px;
    font-weight: bold;
    color: #fff;
    background-color: #007bff;
    border: none;
    border-radius: 5px;
    cursor: pointer;
}

.btn-close:hover {
    background-color: #0056b3;
}

```

</br>

## Html

```html

<template>
    <div class = "container-label">
        Bread Gallery
    </div>
    <div class="gallery">
        <template for:each={products} for:item="product">
            <div key={product.Id} class="pictureItem">
                <img src={product.IMG_Document_Generation__c} alt="Product Image" class="product-image" 
                     onclick={handleProductClick} 
                     data-id={product.Id} 
                     data-name={product.Name} 
                     data-description={product.Description} 
                     data-family={product.Family} 
                     data-price={product.Standard_Price__c} 
                     data-unit={product.Unit_of_Packed__c} 
                     data-image={product.IMG_Document_Generation__c}/>

                <div class="title">
                    <span>{product.Name}</span>
                </div>
            </div>
        </template>
    </div>
    
    <div class="modal" if:true={selectedProductId}>
        <div class="modal-content">
            <div class="modal-header">
                <span class="modal-title">Product Details</span>
                <span class="close" onclick={handleCloseInfo}>×</span>
            </div>

            <div class="modal-body">
                <img src={selectedProductImageURL} alt="Product Image" class="selected-product-image" />
                <div class="description">
                    <span><strong>이름 : </strong> {selectedProductName}</span><br/>
                    <span><strong>상품 설명 : </strong> {selectedProductDescription}</span><br/>
                    <span><strong>분류 : </strong> {selectedProductFamily}</span><br/>
                    <span><strong>표준 가격 : </strong> {selectedProductPrice}</span><br/>
                    <span><strong>단위 : </strong> {selectedProductUnit}</span><br/>
                </div>
            </div>

            <div class="modal-footer">
                <button class="btn-close" onclick={handleCloseInfo}>Close</button>
            </div>
        </div>
    </div>
</template>

```

</br>

## JavaScript

```javascript

import { LightningElement, track } from 'lwc';
import getProducts from '@salesforce/apex/ProductController.getProducts';

export default class Gallery extends LightningElement {
    @track products = [];
    @track selectedProductId;
    @track selectedProductName;
    @track selectedProductDescription;
    @track selectedProductFamily;
    @track selectedProductPrice;
    @track selectedProductUnit;
    @track selectedProductImageURL;

    connectedCallback() {
        this.loadProducts();
    }

    async loadProducts() {
        try {
            const result = await getProducts();
            if (result) {
                this.products = result;
            }
        } catch(error) {
            console.error('Error loading products', error);
        }
    }

    handleProductClick(event) {
        this.selectedProductId = event.currentTarget.dataset.id;
        this.selectedProductName = event.currentTarget.dataset.name;
        this.selectedProductDescription = event.currentTarget.dataset.description;
        this.selectedProductFamily = event.currentTarget.dataset.family;
        this.selectedProductPrice = event.currentTarget.dataset.price;
        this.selectedProductUnit = event.currentTarget.dataset.unit;
        this.selectedProductImageURL = event.currentTarget.dataset.image;
    }

    handleCloseInfo() {
        this.selectedProductId = null;
        this.selectedProductName = null;
        this.selectedProductDescription = null;
        this.selectedProductFamily = null;
        this.selectedProductPrice = null;
        this.selectedProductUnit = null;
        this.selectedProductImageURL = null;
    }
}

```

</br>

## xml 

```xml

<?xml version="1.0" encoding="UTF-8"?>
<LightningComponentBundle xmlns="http://soap.sforce.com/2006/04/metadata" fqn="gallery">
    <apiVersion>52.0</apiVersion>
    <isExposed>true</isExposed>
    <targets>
        <target>lightning__AppPage</target>
        <target>lightning__RecordPage</target>
        <target>lightning__HomePage</target>
    </targets>
</LightningComponentBundle>

```
