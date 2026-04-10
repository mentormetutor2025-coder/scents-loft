# Scents Loft Website — Setup Instructions

## Folder Structure
```
scents-loft/
├── index.html          ← Main website file
├── images/             ← Create this folder and put all product photos here
│   ├── Copy_of_Pink_And_Black_Elegant_Price_List_Instagram_Post__1_.png
│   ├── Zimaya_Fatima_Pink.png
│   ├── Milestone_ALL_YOURS.png
│   └── ... (all other product images)
└── README.md
```

## Step 1 — Images Folder
Create an `images/` folder next to `index.html` and copy all 20+ product photos into it.

## Step 2 — PayFast Setup (Online Payments)
1. Register at https://www.payfast.co.za
2. Get your **merchant_id** and **merchant_key** from your PayFast dashboard
3. Open `index.html`, find this section in the JavaScript (around line 330):
   ```
   merchant_id: '10000100',       ← Replace this
   merchant_key: '46f0cd694581a', ← Replace this
   ```
4. For LIVE payments, change:
   `https://sandbox.payfast.co.za/eng/process`
   to:
   `https://www.payfast.co.za/eng/process`

## Step 3 — WhatsApp (Already Connected!)
The WhatsApp button is already connected to **060 103 3723**.
No extra setup needed — customers can chat directly.

## Step 4 — Adding More Products
Find the `products` array in the `<script>` section and add entries like:
```js
{ id:21, name:'Product Name', brand:'Brand', price:350, gender:'her', size:'100ml', img:'filename.png' },
```
Gender options: `'her'`, `'him'`, `'unisex'`

## Payment Methods Supported
- 💳 Card payments via PayFast (Visa, Mastercard, Amex)
- 🏦 EFT / Instant EFT via PayFast
- 📱 Pay via WhatsApp (sends order details to your WhatsApp)

## Social Links
- Instagram: @Scents_loft → https://instagram.com/scents_loft
- TikTok: Scents Loft (update the TikTok link in the footer)
- WhatsApp: 060 103 3723
