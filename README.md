<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Premium Content Vault • 4 Columns Grid</title>
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
        
        /* Header */
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
            backdrop-filter: blur(5px);
        }
        
        .warning-message {
            background: rgba(255, 193, 7, 0.15);
            border: 1px solid #ffc107;
            color: #ffc107;
            padding: 15px 25px;
            border-radius: 12px;
            max-width: 600px;
            margin: 0 auto 20px;
            font-weight: 500;
            backdrop-filter: blur(10px);
        }
        
        /* Grid de 4 colunas */
        .products-grid {
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            gap: 25px;
            margin: 40px 0;
        }
        
        /* Card do produto */
        .product-card {
            background: rgba(255, 255, 255, 0.05);
            backdrop-filter: blur(12px);
            border: 1px solid rgba(255, 255, 255, 0.1);
            border-radius: 24px;
            padding: 25px 20px;
            transition: all 0.4s cubic-bezier(0.175, 0.885, 0.32, 1.275);
            position: relative;
            overflow: hidden;
            box-shadow: 0 15px 35px rgba(0, 0, 0, 0.3);
        }
        
        .product-card:hover {
            transform: translateY(-12px);
            border-color: #ff4d6d;
            box-shadow: 0 25px 45px rgba(255, 77, 109, 0.25);
            background: rgba(255, 255, 255, 0.1);
        }
        
        /* Container da imagem */
        .product-image {
            width: 100%;
            height: 180px;
            border-radius: 16px;
            overflow: hidden;
            margin-bottom: 20px;
            background: linear-gradient(145deg, #2a2f4f, #1e2338);
            display: flex;
            align-items: center;
            justify-content: center;
            border: 2px solid rgba(255, 255, 255, 0.1);
            transition: all 0.3s;
        }
        
        .product-card:hover .product-image {
            border-color: #ff4d6d;
        }
        
        /* Imagem (pode ser SVG, ícone ou foto) */
        .product-image img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.5s;
        }
        
        .product-card:hover .product-image img {
            transform: scale(1.08);
        }
        
        /* Fallback de ícone (caso não tenha imagem) */
        .image-fallback {
            font-size: 5em;
            filter: drop-shadow(0 10px 15px rgba(0,0,0,0.3));
        }
        
        /* Informações do produto */
        .product-name {
            font-size: 1.4em;
            font-weight: 700;
            color: white;
            margin-bottom: 8px;
            line-height: 1.3;
            min-height: 60px;
            display: -webkit-box;
            -webkit-line-clamp: 2;
            -webkit-box-orient: vertical;
            overflow: hidden;
        }
        
        .product-size {
            color: #a0a8d0;
            font-size: 0.9em;
            margin-bottom: 10px;
            display: flex;
            align-items: center;
            gap: 5px;
        }
        
        .product-size i {
            font-size: 1em;
        }
        
        .product-description {
            color: #b9c0e0;
            font-size: 0.9em;
            margin: 15px 0;
            line-height: 1.5;
            min-height: 45px;
            display: -webkit-box;
            -webkit-line-clamp: 2;
            -webkit-box-orient: vertical;
            overflow: hidden;
        }
        
        .product-price {
            font-size: 2.2em;
            font-weight: 800;
            background: linear-gradient(135deg, #ff4d6d, #ff8fa3);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            margin: 20px 0 15px;
            letter-spacing: 1px;
        }
        
        .btn-buy {
            display: block;
            background: linear-gradient(135deg, #ff4d6d, #d43f5e);
            color: white;
            text-decoration: none;
            padding: 14px 20px;
            border-radius: 50px;
            font-weight: 600;
            text-align: center;
            transition: all 0.3s;
            border: none;
            width: 100%;
            cursor: pointer;
            font-size: 1.1em;
            letter-spacing: 0.5px;
            box-shadow: 0 8px 20px rgba(255, 77, 109, 0.3);
        }
        
        .btn-buy:hover {
            background: linear-gradient(135deg, #ff3355, #c42d4f);
            transform: scale(1.02);
            box-shadow: 0 12px 25px rgba(255, 77, 109, 0.5);
        }
        
        /* Footer */
        .footer {
            text-align: center;
            margin-top: 60px;
            color: rgba(255, 255, 255, 0.3);
            font-size: 0.9em;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
            padding-top: 30px;
        }
        
        /* Responsividade */
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
            <div class="warning-message">
                ⚡ Instant delivery after payment • PayPal & Binance accepted
            </div>
        </div>

        <!-- GRID DE 4 COLUNAS -->
        <div class="products-grid">
            
            <!-- PASTA 1 - BEST SELLERS -->
            <div class="product-card">
                <div class="product-image">
                    <!-- IMAGEM ILUSTRATIVA (SUBSTITUA PELO LINK DA SUA IMAGEM) -->
                    <img src="https://via.placeholder.com/300x180/2a2f4f/ff4d6d?text=BEST+SELLERS" alt="Best Sellers">
                    <!-- Se preferir ícone em vez de imagem, use isto:
                    <div class="image-fallback">📁🔥</div>
                    -->
                </div>
                <div class="product-name">BEST SELLERS AND RAREST E404 🏆</div>
                <div class="product-size"><span>📦</span> 14.29 GB</div>
                <div class="product-description">Coleção completa dos mais vendidos e raros. Edição limitada.</div>
                <div class="product-price">$29.99</div>
                <a href="#" class="btn-buy">Buy Now via PayPal</a>
                <!-- Link alternativo Binance 
                <a href="#" class="btn-buy" style="margin-top: 10px; background: linear-gradient(135deg, #f0b90b, #cc9b08);">Buy with Binance</a>
                -->
            </div>
            
            <!-- PASTA 2 - BOP SLUTS -->
            <div class="product-card">
                <div class="product-image">
                    <img src="https://via.placeholder.com/300x180/2a2f4f/ff4d6d?text=BOP+SLUTS" alt="Bop Sluts">
                </div>
                <div class="product-name">bop sluts</div>
                <div class="product-size"><span>📦</span> 1.04 TB</div>
                <div class="product-description">Mega coleção premium. Qualidade 4K. Atualizado.</div>
                <div class="product-price">$49.99</div>
                <a href="#" class="btn-buy">Buy Now via PayPal</a>
            </div>
            
            <!-- PASTA 3 - C P MEGA PREMIUM -->
            <div class="product-card">
                <div class="product-image">
                    <img src="https://via.placeholder.com/300x180/2a2f4f/ff4d6d?text=MEGA+PREMIUM" alt="Mega Premium">
                </div>
                <div class="product-name">C P - MEGA PREMIUM 7K</div>
                <div class="product-size"><span>📦</span> 446.9 MB</div>
                <div class="product-description">Pacote premium 7K. Material selecionado.</div>
                <div class="product-price">$19.99</div>
                <a href="#" class="btn-buy">Buy Now via PayPal</a>
            </div>
            
            <!-- PASTA 4 - C P COLLECTION -->
            <div class="product-card">
                <div class="product-image">
                    <img src="https://via.placeholder.com/300x180/2a2f4f/ff4d6d?text=COLLECTION+PRO" alt="Collection Pro">
                </div>
                <div class="product-name">C P COLLETION PRO 1.4K</div>
                <div class="product-size"><span>📦</span> 297.72 GB</div>
                <div class="product-description">Coleção profissional 1.4K. Organizado.</div>
                <div class="product-price">$39.99</div>
                <a href="#" class="btn-buy">Buy Now via PayPal</a>
            </div>
            
            <!-- PASTA 5 - F4F -->
            <div class="product-card">
                <div class="product-image">
                    <img src="https://via.placeholder.com/300x180/2a2f4f/ff4d6d?text=F4F" alt="F4F">
                </div>
                <div class="product-name">f4f</div>
                <div class="product-size"><span>📦</span> 17.71 GB</div>
                <div class="product-description">Pacote exclusivo F4F. Conteúdo selecionado.</div>
                <div class="product-price">$14.99</div>
                <a href="#" class="btn-buy">Buy Now via PayPal</a>
            </div>
            
            <!-- PASTA 6 - MY C P -->
            <div class="product-card">
                <div class="product-image">
                    <img src="https://via.placeholder.com/300x180/2a2f4f/ff4d6d?text=MY+CP" alt="My CP">
                </div>
                <div class="product-name">MY C P us E404</div>
                <div class="product-size"><span>📦</span> 11.11 GB</div>
                <div class="product-description">Coleção pessoal. Raro e exclusivo.</div>
                <div class="product-price">$34.99</div>
                <a href="#" class="btn-buy">Buy Now via PayPal</a>
            </div>
            
            <!-- PASTA 7 - EXTRA (exemplo) -->
            <div class="product-card">
                <div class="product-image">
                    <img src="https://via.placeholder.com/300x180/2a2f4f/ff4d6d?text=VIP+ONLY" alt="VIP Only">
                </div>
                <div class="product-name">VIP ONLY - LIMITED</div>
                <div class="product-size"><span>📦</span> 45.2 GB</div>
                <div class="product-description">Conteúdo VIP limitado. Apenas para membros.</div>
                <div class="product-price">$59.99</div>
                <a href="#" class="btn-buy">Buy Now via PayPal</a>
            </div>
            
            <!-- PASTA 8 - EXTRA 2 -->
            <div class="product-card">
                <div class="product-image">
                    <img src="https://via.placeholder.com/300x180/2a2f4f/ff4d6d?text=4K+COLLECTION" alt="4K Collection">
                </div>
                <div class="product-name">4K ULTRA HD COLLECTION</div>
                <div class="product-size"><span>📦</span> 89.3 GB</div>
                <div class="product-description">Tudo em 4K. Qualidade máxima.</div>
                <div class="product-price">$44.99</div>
                <a href="#" class="btn-buy">Buy Now via PayPal</a>
            </div>
        </div>

        <div class="footer">
            <p>© 2026 Premium Content Vault • All rights reserved • 18+ Only</p>
            <p style="margin-top: 10px; font-size: 0.85em;">🔒 Secure payment • Instant delivery • No refunds on digital items</p>
        </div>
    </div>
</body>
</html>
