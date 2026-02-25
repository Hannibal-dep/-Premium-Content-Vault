<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Premium Vault • 50+ Exclusive Packs</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Segoe UI', Roboto, system-ui, sans-serif;
            background: linear-gradient(145deg, #0b0c1a 0%, #1a1f35 100%);
            min-height: 100vh;
            padding: 40px 20px;
        }
        
        .container {
            max-width: 1400px;
            margin: 0 auto;
        }
        
        .header {
            text-align: center;
            margin-bottom: 50px;
        }
        
        .header h1 {
            font-size: 3em;
            background: linear-gradient(135deg, #fff 0%, #a5b4fc 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            margin-bottom: 15px;
            letter-spacing: 2px;
        }
        
        .badge {
            display: inline-block;
            background: #ff4d6d;
            color: white;
            padding: 8px 30px;
            border-radius: 50px;
            font-weight: 600;
            font-size: 1.1em;
            box-shadow: 0 10px 20px rgba(255, 77, 109, 0.3);
            margin-bottom: 20px;
            border: 1px solid rgba(255,255,255,0.2);
        }
        
        .stats {
            background: rgba(255, 255, 255, 0.05);
            padding: 15px;
            border-radius: 50px;
            max-width: 300px;
            margin: 0 auto 30px;
            color: white;
            font-size: 1.1em;
            border: 1px solid rgba(255,255,255,0.1);
        }
        
        .info-message {
            background: rgba(76, 175, 80, 0.15);
            border: 1px solid #4caf50;
            color: #4caf50;
            padding: 15px 25px;
            border-radius: 12px;
            max-width: 700px;
            margin: 0 auto 20px;
            font-weight: 500;
        }
        
        .products-grid {
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            gap: 25px;
            margin: 40px 0;
        }
        
        .product-card {
            background: rgba(255, 255, 255, 0.05);
            backdrop-filter: blur(12px);
            border: 1px solid rgba(255, 255, 255, 0.1);
            border-radius: 24px;
            padding: 25px 20px;
            transition: all 0.4s;
            position: relative;
            box-shadow: 0 15px 35px rgba(0, 0, 0, 0.3);
        }
        
        .product-card:hover {
            transform: translateY(-12px);
            border-color: #4caf50;
            box-shadow: 0 25px 45px rgba(76, 175, 80, 0.25);
            background: rgba(255, 255, 255, 0.1);
        }
        
        .product-image {
            width: 100%;
            height: 160px;
            border-radius: 16px;
            overflow: hidden;
            margin-bottom: 20px;
            background: linear-gradient(145deg, #2a2f4f, #1e2338);
            display: flex;
            align-items: center;
            justify-content: center;
            border: 2px solid rgba(255, 255, 255, 0.1);
        }
        
        .product-card:hover .product-image {
            border-color: #4caf50;
        }
        
        .product-image img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.5s;
        }
        
        .product-card:hover .product-image img {
            transform: scale(1.08);
        }
        
        .product-name {
            font-size: 1.2em;
            font-weight: 700;
            color: white;
            margin-bottom: 8px;
            line-height: 1.3;
            min-height: 50px;
            display: -webkit-box;
            -webkit-line-clamp: 2;
            -webkit-box-orient: vertical;
            overflow: hidden;
        }
        
        .product-size {
            color: #a0a8d0;
            font-size: 0.85em;
            margin-bottom: 8px;
            display: flex;
            align-items: center;
            gap: 5px;
        }
        
        .product-description {
            color: #b9c0e0;
            font-size: 0.85em;
            margin: 10px 0;
            line-height: 1.4;
            min-height: 40px;
            display: -webkit-box;
            -webkit-line-clamp: 2;
            -webkit-box-orient: vertical;
            overflow: hidden;
        }
        
        .product-price {
            font-size: 1.8em;
            font-weight: 800;
            background: linear-gradient(135deg, #4caf50, #8bc34a);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            margin: 15px 0 10px;
        }
        
        .btn-gumroad {
            display: block;
            background: linear-gradient(135deg, #ff90e8, #ff4d6d);
            color: white;
            text-decoration: none;
            padding: 12px 15px;
            border-radius: 50px;
            font-weight: 600;
            text-align: center;
            transition: all 0.3s;
            width: 100%;
            font-size: 0.95em;
            box-shadow: 0 8px 20px rgba(255, 77, 109, 0.3);
        }
        
        .btn-gumroad:hover {
            background: linear-gradient(135deg, #ff7ad0, #ff3355);
            transform: scale(1.02);
        }
        
        .footer {
            text-align: center;
            margin-top: 60px;
            color: rgba(255, 255, 255, 0.3);
            font-size: 0.9em;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
            padding-top: 30px;
        }
        
        @media (max-width: 1100px) {
            .products-grid {
                grid-template-columns: repeat(3, 1fr);
            }
        }
        
        @media (max-width: 800px) {
            .products-grid {
                grid-template-columns: repeat(2, 1fr);
            }
        }
        
        @media (max-width: 500px) {
            .products-grid {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="header">
            <h1>✦ PREMIUM VAULT ✦</h1>
            <div class="badge">🔞 18+ ONLY • VERIFY AGE</div>
            <div class="stats">📦 50+ Exclusive Packs • Total: XX TB</div>
            <div class="info-message">
                ⚡ Instant delivery via Gumroad • Secure checkout • PayPal & Cards accepted
            </div>
        </div>

        <div class="products-grid">
            
            <!-- ========================================== -->
            <!-- COMEÇO DOS 50 PRODUTOS - REPITA ESTE BLOCO 50 VEZES -->
            <!-- ========================================== -->
            
            <!-- PRODUTO 1 -->
            <div class="product-card">
                <div class="product-image">
                    <img src="https://via.placeholder.com/300x160/2a2f4f/4caf50?text=PACK+001" alt="Pack 001">
                </div>
                <div class="product-name">[NOME EXATO DA PASTA 1]</div>
                <div class="product-size"><span>📦</span> [TAMANHO] GB</div>
                <div class="product-description">[DESCRIÇÃO EM INGLÊS] Premium content pack. 18+ only.</div>
                <div class="product-price">$[PREÇO]</div>
                <a href="[LINK-GUMROAD-PRODUTO-1]" class="btn-gumroad" target="_blank">Buy Now</a>
            </div>
            
            <!-- PRODUTO 2 -->
            <div class="product-card">
                <div class="product-image">
                    <img src="https://via.placeholder.com/300x160/2a2f4f/4caf50?text=PACK+002" alt="Pack 002">
                </div>
                <div class="product-name">[NOME EXATO DA PASTA 2]</div>
                <div class="product-size"><span>📦</span> [TAMANHO] GB</div>
                <div class="product-description">[DESCRIÇÃO EM INGLÊS] Premium content pack. 18+ only.</div>
                <div class="product-price">$[PREÇO]</div>
                <a href="[LINK-GUMROAD-PRODUTO-2]" class="btn-gumroad" target="_blank">Buy Now</a>
            </div>
            
            <!-- CONTINUE REPETINDO ATÉ O PRODUTO 50 -->
            
            <!-- EXEMPLO PRODUTO 50 -->
            <div class="product-card">
                <div class="product-image">
                    <img src="https://via.placeholder.com/300x160/2a2f4f/4caf50?text=PACK+050" alt="Pack 050">
                </div>
                <div class="product-name">[NOME EXATO DA PASTA 50]</div>
                <div class="product-size"><span>📦</span> [TAMANHO] GB</div>
                <div class="product-description">[DESCRIÇÃO EM INGLÊS] Premium content pack. 18+ only.</div>
                <div class="product-price">$[PREÇO]</div>
                <a href="[LINK-GUMROAD-PRODUTO-50]" class="btn-gumroad" target="_blank">Buy Now</a>
            </div>
            
            <!-- ========================================== -->
            <!-- FIM DOS 50 PRODUTOS -->
            <!-- ========================================== -->
            
        </div>

        <div class="footer">
            <p>© 2026 Premium Content Vault • 50+ Exclusive Packs • 18+ Only</p>
            <p style="margin-top: 10px; font-size: 0.85em;">🔒 Secure payment via Gumroad • Instant delivery • PayPal & cards accepted • No refunds on digital items</p>
        </div>
    </div>
</body>
</html>
