<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Premium Content Vault</title>
    <style>
        * { margin: 0; padding: 0; box-sizing: border-box; }
        body {
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;
            background: linear-gradient(135deg, #1a1a2e 0%, #16213e 100%);
            min-height: 100vh;
            padding: 40px 20px;
        }
        .container {
            max-width: 1400px;
            margin: 0 auto;
        }
        h1 {
            color: white;
            font-size: 2.5em;
            margin-bottom: 10px;
            text-align: center;
        }
        .badge {
            background: #e94560;
            color: white;
            padding: 8px 20px;
            border-radius: 30px;
            display: inline-block;
            margin: 0 auto 40px;
            font-weight: bold;
            text-align: center;
            width: fit-content;
            display: block;
        }
        .products-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(320px, 1fr));
            gap: 25px;
            margin-top: 30px;
        }
        .product-card {
            background: rgba(255, 255, 255, 0.95);
            border-radius: 20px;
            padding: 25px;
            transition: all 0.3s;
            box-shadow: 0 10px 30px rgba(0,0,0,0.2);
            border: 1px solid rgba(255,255,255,0.1);
            backdrop-filter: blur(10px);
        }
        .product-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 20px 40px rgba(233, 69, 96, 0.3);
            border-color: #e94560;
        }
        .product-icon {
            font-size: 2.5em;
            margin-bottom: 15px;
        }
        .product-name {
            font-size: 1.5em;
            font-weight: bold;
            color: #1a1a2e;
            margin-bottom: 10px;
            word-break: break-word;
        }
        .product-size {
            color: #666;
            font-size: 0.9em;
            margin-bottom: 15px;
            padding-bottom: 15px;
            border-bottom: 1px solid #eee;
        }
        .product-price {
            font-size: 2.2em;
            font-weight: bold;
            color: #e94560;
            margin: 20px 0;
        }
        .btn {
            display: block;
            background: linear-gradient(135deg, #e94560 0%, #0f3460 100%);
            color: white;
            text-decoration: none;
            padding: 15px;
            border-radius: 50px;
            font-weight: bold;
            transition: opacity 0.3s;
            text-align: center;
            border: none;
            width: 100%;
            cursor: pointer;
        }
        .btn:hover {
            opacity: 0.9;
        }
        .warning {
            background: rgba(233, 69, 96, 0.2);
            border: 1px solid #e94560;
            color: white;
            padding: 15px;
            border-radius: 10px;
            margin: 30px 0 20px;
            font-size: 0.95em;
            text-align: center;
        }
        .footer {
            text-align: center;
            margin-top: 50px;
            color: rgba(255,255,255,0.5);
            font-size: 0.9em;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>✨ PREMIUM CONTENT VAULT</h1>
        <div class="badge">🔞 VERIFY AGE • 18+ ONLY</div>

        <div class="warning">
            ⚡ Instant delivery after payment • Secure via PayPal & Binance
        </div>

        <div class="products-grid">
            <!-- PASTA 1: Substitua os dados abaixo -->
            <div class="product-card">
                <div class="product-icon">📁</div>
                <div class="product-name">Nome da Pasta 1</div>
                <div class="product-size">Tamanho: XX GB</div>
                <p>Descrição opcional do conteúdo...</p>
                <div class="product-price">$19.99</div>
                <a href="LINK-DO-PRODUTO-NO-GUMROAD-OU-SEU-SITE" class="btn" target="_blank">
                    Buy Now
                </a>
            </div>

            <!-- PASTA 2 -->
            <div class="product-card">
                <div class="product-icon">📁</div>
                <div class="product-name">Nome da Pasta 2</div>
                <div class="product-size">Tamanho: XX GB</div>
                <p>Descrição opcional do conteúdo...</p>
                <div class="product-price">$29.99</div>
                <a href="LINK-DO-PRODUTO-NO-GUMROAD-OU-SEU-SITE" class="btn" target="_blank">
                    Buy Now
                </a>
            </div>

            <!-- ADICIONE MAIS PASTAS AQUI, seguindo o mesmo padrão -->
        </div>

        <div class="footer">
            © 2026 Premium Content Vault • All rights reserved
        </div>
    </div>
</body>
</html>
