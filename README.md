
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Huellitas Alegres - Cuidado y Amor para tu Mascota</title>
    <meta name="description" content="Huellitas Alegres - Servicios profesionales de cuidado para mascotas en Bocagrande, Cartagena. Baño, corte, veterinaria y productos para tu perro.">
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
    <style>
/* Reset y configuración base */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

html {
    scroll-behavior: smooth;
}

body {
    font-family: 'Inter', sans-serif;
    line-height: 1.6;
    color: #333;
    background-color: #fff;
}

.container {
    max-width: 1200px;
    margin: 0 auto;
    padding: 0 20px;
}

/* Navegación */
.navbar {
    position: fixed;
    top: 0;
    width: 100%;
    background: rgba(255, 255, 255, 0.95);
    backdrop-filter: blur(10px);
    z-index: 1000;
    padding: 1rem 0;
    box-shadow: 0 2px 20px rgba(0, 0, 0, 0.1);
}

.nav-container {
    max-width: 1200px;
    margin: 0 auto;
    padding: 0 20px;
    display: flex;
    justify-content: space-between;
    align-items: center;
}

.nav-logo a {
    font-size: 1.5rem;
    font-weight: 700;
    color: #ff6b35;
    text-decoration: none;
    display: flex;
    align-items: center;
    gap: 0.5rem;
}

.nav-logo i {
    font-size: 1.8rem;
}

.nav-menu {
    display: flex;
    list-style: none;
    gap: 2rem;
    align-items: center;
}

.nav-link {
    text-decoration: none;
    color: #333;
    font-weight: 500;
    transition: color 0.3s ease;
    position: relative;
}

.nav-link:hover {
    color: #ff6b35;
}

.nav-link::after {
    content: '';
    position: absolute;
    width: 0;
    height: 2px;
    bottom: -5px;
    left: 0;
    background-color: #ff6b35;
    transition: width 0.3s ease;
}

.nav-link:hover::after {
    width: 100%;
}

.cart-icon {
    position: relative;
    cursor: pointer;
    font-size: 1.5rem;
    color: #ff6b35;
    transition: transform 0.3s ease;
}

.cart-icon:hover {
    transform: scale(1.1);
}

.cart-count {
    position: absolute;
    top: -8px;
    right: -8px;
    background: #e74c3c;
    color: white;
    border-radius: 50%;
    width: 20px;
    height: 20px;
    display: none;
    align-items: center;
    justify-content: center;
    font-size: 0.8rem;
    font-weight: 600;
    min-width: 20px;
}

.nav-toggle {
    display: none;
    flex-direction: column;
    cursor: pointer;
}

.bar {
    width: 25px;
    height: 3px;
    background-color: #333;
    margin: 3px 0;
    transition: 0.3s;
}

/* Carrito de Compras */
.cart-sidebar {
    position: fixed;
    top: 0;
    right: -400px;
    width: 400px;
    height: 100vh;
    background: white;
    box-shadow: -5px 0 15px rgba(0, 0, 0, 0.1);
    z-index: 1001;
    transition: right 0.3s ease;
    overflow-y: auto;
}

.cart-sidebar.active {
    right: 0;
}

.cart-header {
    padding: 2rem;
    border-bottom: 1px solid #eee;
    display: flex;
    justify-content: space-between;
    align-items: center;
}

.cart-header h3 {
    color: #2c3e50;
    font-size: 1.5rem;
}

.cart-close {
    background: none;
    border: none;
    font-size: 1.5rem;
    cursor: pointer;
    color: #7f8c8d;
}

.cart-items {
    padding: 1rem 2rem;
    max-height: 60vh;
    overflow-y: auto;
}

.cart-item {
    display: flex;
    align-items: center;
    gap: 1rem;
    padding: 1rem 0;
    border-bottom: 1px solid #f1f2f6;
}

.cart-item-image {
    width: 60px;
    height: 60px;
    border-radius: 8px;
    overflow: hidden;
    flex-shrink: 0;
    background: #f8f9fa;
    display: flex;
    align-items: center;
    justify-content: center;
}

.cart-item-image img {
    width: 100%;
    height: 100%;
    object-fit: cover;
}

.cart-item-image .fallback-icon {
    color: #ff6b35;
    font-size: 1.5rem;
}

.cart-item-info {
    flex: 1;
}

.cart-item-name {
    font-weight: 600;
    color: #2c3e50;
    margin-bottom: 0.3rem;
    font-size: 0.9rem;
}

.cart-item-price {
    color: #ff6b35;
    font-weight: 600;
    font-size: 0.9rem;
}

.cart-item-controls {
    display: flex;
    align-items: center;
    gap: 0.5rem;
    margin-top: 0.5rem;
}

.quantity-btn {
    width: 30px;
    height: 30px;
    border: 1px solid #ddd;
    background: white;
    border-radius: 4px;
    cursor: pointer;
    display: flex;
    align-items: center;
    justify-content: center;
    font-weight: 600;
}

.quantity-btn:hover {
    background: #f8f9fa;
}

.quantity-display {
    min-width: 40px;
    text-align: center;
    font-weight: 600;
}

.remove-item {
    background: none;
    border: none;
    color: #e74c3c;
    cursor: pointer;
    font-size: 1.2rem;
    margin-left: 0.5rem;
}

.cart-footer {
    padding: 2rem;
    border-top: 1px solid #eee;
    background: #f8f9fa;
}

.cart-total {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-bottom: 1.5rem;
    font-size: 1.2rem;
    font-weight: 700;
}

.cart-total-price {
    color: #ff6b35;
    font-size: 1.5rem;
}

.cart-checkout {
    width: 100%;
    background: linear-gradient(135deg, #ff6b35, #ffa726);
    color: white;
    border: none;
    padding: 1rem;
    border-radius: 8px;
    font-weight: 600;
    font-size: 1.1rem;
    cursor: pointer;
    transition: transform 0.3s ease;
}

.cart-checkout:hover {
    transform: translateY(-2px);
}

.cart-empty {
    text-align: center;
    padding: 3rem 2rem;
    color: #7f8c8d;
}

.cart-empty i {
    font-size: 3rem;
    margin-bottom: 1rem;
    color: #bdc3c7;
}

.cart-overlay {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: rgba(0, 0, 0, 0.5);
    z-index: 1000;
    opacity: 0;
    visibility: hidden;
    transition: all 0.3s ease;
}

.cart-overlay.active {
    opacity: 1;
    visibility: visible;
}

/* Sección Hero */
.hero {
    padding: 120px 0 80px;
    background: linear-gradient(135deg, #fff5f0 0%, #ffe8d6 100%);
    min-height: 100vh;
    display: flex;
    align-items: center;
}

.hero-container {
    max-width: 1200px;
    margin: 0 auto;
    padding: 0 20px;
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 4rem;
    align-items: center;
}

.hero-title {
    font-size: 3.5rem;
    font-weight: 700;
    line-height: 1.2;
    margin-bottom: 1rem;
    color: #2c3e50;
}

.highlight {
    color: #ff6b35;
    position: relative;
}

.highlight::after {
    content: '';
    position: absolute;
    bottom: 0;
    left: 0;
    width: 100%;
    height: 3px;
    background: linear-gradient(90deg, #ff6b35, #ffa726);
    border-radius: 2px;
}

.hero-subtitle {
    font-size: 1.5rem;
    color: #7f8c8d;
    margin-bottom: 1.5rem;
    font-weight: 500;
}

.hero-description {
    font-size: 1.1rem;
    color: #5d6d7e;
    margin-bottom: 2.5rem;
    line-height: 1.7;
}

.hero-buttons {
    display: flex;
    gap: 1rem;
    flex-wrap: wrap;
}

.btn {
    padding: 12px 30px;
    border-radius: 50px;
    text-decoration: none;
    font-weight: 600;
    transition: all 0.3s ease;
    border: 2px solid transparent;
    display: inline-block;
    text-align: center;
}

.btn-primary {
    background: linear-gradient(135deg, #ff6b35, #ffa726);
    color: white;
    box-shadow: 0 4px 15px rgba(255, 107, 53, 0.3);
}

.btn-primary:hover {
    transform: translateY(-2px);
    box-shadow: 0 6px 20px rgba(255, 107, 53, 0.4);
}

.btn-secondary {
    background: transparent;
    color: #ff6b35;
    border: 2px solid #ff6b35;
}

.btn-secondary:hover {
    background: #ff6b35;
    color: white;
    transform: translateY(-2px);
}

.hero-image {
    display: flex;
    justify-content: center;
    align-items: center;
}

.hero-avatar {
    width: 350px;
    height: 350px;
    border-radius: 50%;
    overflow: hidden;
    box-shadow: 0 20px 40px rgba(0, 0, 0, 0.1);
    border: 8px solid white;
    position: relative;
    background: linear-gradient(45deg, #ff6b35, #ffa726);
    display: flex;
    align-items: center;
    justify-content: center;
}

.hero-avatar::before {
    content: '';
    position: absolute;
    top: -10px;
    left: -10px;
    right: -10px;
    bottom: -10px;
    background: linear-gradient(45deg, #ff6b35, #ffa726, #ff6b35);
    border-radius: 50%;
    z-index: -1;
    animation: rotate 3s linear infinite;
}

@keyframes rotate {
    0% { transform: rotate(0deg); }
    100% { transform: rotate(360deg); }
}

.hero-avatar img {
    width: 100%;
    height: 100%;
    object-fit: cover;
    border-radius: 50%;
}

.hero-avatar .fallback-icon {
    font-size: 8rem;
    color: white;
    text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.3);
}

/* Secciones generales */
.section-header {
    text-align: center;
    margin-bottom: 4rem;
}

.section-title {
    font-size: 2.5rem;
    font-weight: 700;
    color: #2c3e50;
    margin-bottom: 1rem;
    position: relative;
}

.section-title::after {
    content: '';
    position: absolute;
    bottom: -10px;
    left: 50%;
    transform: translateX(-50%);
    width: 60px;
    height: 3px;
    background: linear-gradient(90deg, #ff6b35, #ffa726);
    border-radius: 2px;
}

.section-subtitle {
    font-size: 1.2rem;
    color: #7f8c8d;
    max-width: 600px;
    margin: 0 auto;
}

/* Sección About */
.about {
    padding: 80px 0;
    background: #f8f9fa;
}

.about-content {
    display: grid;
    grid-template-columns: 2fr 1fr;
    gap: 4rem;
    align-items: start;
}

.about-text p {
    font-size: 1.1rem;
    color: #5d6d7e;
    margin-bottom: 1.5rem;
    line-height: 1.8;
}

.skills {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 1.5rem;
    margin-top: 2rem;
}

.skill-item {
    display: flex;
    align-items: center;
    gap: 0.8rem;
    padding: 1rem;
    background: white;
    border-radius: 10px;
    box-shadow: 0 5px 15px rgba(0, 0, 0, 0.08);
    transition: transform 0.3s ease;
}

.skill-item:hover {
    transform: translateY(-3px);
}

.skill-item i {
    font-size: 1.5rem;
    color: #ff6b35;
}

.skill-item span {
    font-weight: 600;
    color: #2c3e50;
}

.about-stats {
    display: flex;
    flex-direction: column;
    gap: 2rem;
}

.stat-item {
    text-align: center;
    padding: 2rem;
    background: white;
    border-radius: 15px;
    box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
    transition: transform 0.3s ease;
}

.stat-item:hover {
    transform: translateY(-5px);
}

.stat-item h3 {
    font-size: 2.5rem;
    font-weight: 700;
    color: #ff6b35;
    margin-bottom: 0.5rem;
}

.stat-item p {
    color: #7f8c8d;
    font-weight: 500;
}

/* Sección Services */
.services {
    padding: 80px 0;
    background: white;
}

.services-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
    gap: 2rem;
}

.service-card {
    background: white;
    padding: 2.5rem 2rem;
    border-radius: 15px;
    text-align: center;
    box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
    transition: all 0.3s ease;
    border: 1px solid #f1f2f6;
}

.service-card:hover {
    transform: translateY(-10px);
    box-shadow: 0 20px 40px rgba(0, 0, 0, 0.15);
}

.service-icon {
    width: 80px;
    height: 80px;
    background: linear-gradient(135deg, #ff6b35, #ffa726);
    border-radius: 50%;
    display: flex;
    align-items: center;
    justify-content: center;
    margin: 0 auto 1.5rem;
}

.service-icon i {
    font-size: 2rem;
    color: white;
}

.service-card h3 {
    font-size: 1.5rem;
    font-weight: 600;
    color: #2c3e50;
    margin-bottom: 1rem;
}

.service-card p {
    color: #7f8c8d;
    line-height: 1.6;
}

/* Sección Tienda */
.shop {
    padding: 80px 0;
    background: #f8f9fa;
}

.shop-categories {
    display: flex;
    justify-content: center;
    gap: 1rem;
    margin-bottom: 3rem;
    flex-wrap: wrap;
}

.category-filter {
    padding: 0.8rem 1.5rem;
    background: #fff;
    border: 2px solid #e9ecef;
    border-radius: 25px;
    color: #7f8c8d;
    text-decoration: none;
    font-weight: 600;
    transition: all 0.3s ease;
    cursor: pointer;
}

.category-filter:hover,
.category-filter.active {
    background: #ff6b35;
    color: white;
    border-color: #ff6b35;
}

.shop-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
    gap: 2rem;
}

.product-card {
    background: white;
    border-radius: 15px;
    overflow: hidden;
    box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
    transition: all 0.3s ease;
    border: 1px solid #f1f2f6;
}

.product-card:hover {
    transform: translateY(-10px);
    box-shadow: 0 20px 40px rgba(0, 0, 0, 0.15);
}

.product-image {
    height: 200px;
    overflow: hidden;
    position: relative;
    background: #f8f9fa;
    display: flex;
    align-items: center;
    justify-content: center;
}

.product-image img {
    width: 100%;
    height: 100%;
    object-fit: cover;
    transition: transform 0.3s ease;
}

.product-card:hover .product-image img {
    transform: scale(1.1);
}

.product-image .fallback-icon {
    font-size: 4rem;
    color: #ff6b35;
}

.product-badge {
    position: absolute;
    top: 10px;
    right: 10px;
    background: linear-gradient(135deg, #ff6b35, #ffa726);
    color: white;
    padding: 0.3rem 0.8rem;
    border-radius: 15px;
    font-size: 0.8rem;
    font-weight: 600;
}

.product-info {
    padding: 1.5rem;
}

.product-category {
    color: #ff6b35;
    font-size: 0.9rem;
    font-weight: 600;
    text-transform: uppercase;
    margin-bottom: 0.5rem;
}

.product-name {
    font-size: 1.3rem;
    font-weight: 600;
    color: #2c3e50;
    margin-bottom: 0.8rem;
}

.product-description {
    color: #7f8c8d;
    font-size: 0.95rem;
    line-height: 1.5;
    margin-bottom: 1rem;
}

.product-price {
    display: flex;
    align-items: center;
    justify-content: space-between;
    margin-bottom: 1rem;
}

.price-current {
    font-size: 1.5rem;
    font-weight: 700;
    color: #ff6b35;
}

.price-original {
    font-size: 1.1rem;
    color: #95a5a6;
    text-decoration: line-through;
}

.product-actions {
    display: flex;
    gap: 0.5rem;
}

.btn-cart {
    flex: 1;
    background: linear-gradient(135deg, #ff6b35, #ffa726);
    color: white;
    border: none;
    padding: 0.8rem 1rem;
    border-radius: 8px;
    font-weight: 600;
    cursor: pointer;
    transition: all 0.3s ease;
    text-decoration: none;
    text-align: center;
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 0.5rem;
}

.btn-cart:hover {
    transform: translateY(-2px);
    box-shadow: 0 5px 15px rgba(255, 107, 53, 0.3);
}

.btn-wishlist {
    width: 45px;
    height: 45px;
    background: #f8f9fa;
    border: 2px solid #e9ecef;
    border-radius: 8px;
    display: flex;
    align-items: center;
    justify-content: center;
    color: #7f8c8d;
    cursor: pointer;
    transition: all 0.3s ease;
}

.btn-wishlist:hover {
    background: #ff6b35;
    color: white;
    border-color: #ff6b35;
}

/* Sección Precios */
.prices {
    padding: 80px 0;
    background: white;
}

.prices-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
    gap: 2rem;
    margin-bottom: 4rem;
}

.price-card {
    background: white;
    border-radius: 20px;
    padding: 2.5rem 2rem;
    text-align: center;
    box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
    transition: all 0.3s ease;
    position: relative;
    border: 2px solid transparent;
}

.price-card:hover {
    transform: translateY(-10px);
    box-shadow: 0 20px 40px rgba(0, 0, 0, 0.15);
}

.price-card.featured {
    border: 2px solid #ff6b35;
    transform: scale(1.05);
}

.price-card.featured:hover {
    transform: scale(1.05) translateY(-10px);
}

.price-badge {
    position: absolute;
    top: -15px;
    left: 50%;
    transform: translateX(-50%);
    background: linear-gradient(135deg, #ff6b35, #ffa726);
    color: white;
    padding: 0.5rem 1.5rem;
    border-radius: 20px;
    font-size: 0.9rem;
    font-weight: 600;
}

.price-header h3 {
    font-size: 1.8rem;
    font-weight: 700;
    color: #2c3e50;
    margin-bottom: 1rem;
}

.price {
    display: flex;
    align-items: center;
    justify-content: center;
    margin-bottom: 1rem;
}

.currency {
    font-size: 1.5rem;
    color: #ff6b35;
    font-weight: 600;
}

.amount {
    font-size: 3rem;
    font-weight: 700;
    color: #2c3e50;
    margin-left: 0.2rem;
}

.price-description {
    color: #7f8c8d;
    margin-bottom: 2rem;
    font-style: italic;
}

.price-features {
    list-style: none;
    padding: 0;
    margin-bottom: 2rem;
}

.price-features li {
    padding: 0.8rem 0;
    border-bottom: 1px solid #f1f2f6;
    display: flex;
    align-items: center;
    gap: 0.8rem;
}

.price-features li:last-child {
    border-bottom: none;
}

.price-features i {
    color: #27ae60;
    font-size: 1.1rem;
}

.btn-outline {
    background: transparent;
    color: #ff6b35;
    border: 2px solid #ff6b35;
    padding: 12px 30px;
    border-radius: 50px;
    text-decoration: none;
    font-weight: 600;
    transition: all 0.3s ease;
    display: inline-block;
}

.btn-outline:hover {
    background: #ff6b35;
    color: white;
    transform: translateY(-2px);
}

.additional-services {
    background: #f8f9fa;
    padding: 2.5rem;
    border-radius: 15px;
    box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
}

.additional-services h3 {
    text-align: center;
    font-size: 1.8rem;
    color: #2c3e50;
    margin-bottom: 2rem;
}

.additional-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
    gap: 1.5rem;
}

.additional-item {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 1.5rem;
    background: white;
    border-radius: 10px;
    border-left: 4px solid #ff6b35;
}

.service-name {
    font-weight: 600;
    color: #2c3e50;
}

.service-price {
    font-weight: 700;
    color: #ff6b35;
    font-size: 1.1rem;
}

/* Sección Portfolio */
.portfolio {
    padding: 80px 0;
    background: #f8f9fa;
}

.portfolio-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
    gap: 2rem;
}

.portfolio-item {
    border-radius: 15px;
    overflow: hidden;
    box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
    transition: transform 0.3s ease;
    background: white;
}

.portfolio-item:hover {
    transform: translateY(-5px);
}

.portfolio-image {
    position: relative;
    overflow: hidden;
    height: 250px;
    background: #f8f9fa;
    display: flex;
    align-items: center;
    justify-content: center;
}

.portfolio-image img {
    width: 100%;
    height: 100%;
    object-fit: cover;
    transition: transform 0.3s ease;
}

.portfolio-item:hover .portfolio-image img {
    transform: scale(1.1);
}

.portfolio-image .fallback-icon {
    font-size: 5rem;
    color: #ff6b35;
}

.portfolio-overlay {
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    background: rgba(255, 107, 53, 0.9);
    display: flex;
    align-items: center;
    justify-content: center;
    opacity: 0;
    transition: opacity 0.3s ease;
}

.portfolio-item:hover .portfolio-overlay {
    opacity: 1;
}

.portfolio-info {
    text-align: center;
    color: white;
    padding: 2rem;
}

.portfolio-info h4 {
    font-size: 1.5rem;
    font-weight: 600;
    margin-bottom: 0.5rem;
}

.portfolio-info p {
    margin-bottom: 1rem;
    opacity: 0.9;
}

.portfolio-link {
    color: white;
    font-size: 1.5rem;
    text-decoration: none;
    transition: transform 0.3s ease;
}

.portfolio-link:hover {
    transform: scale(1.2);
}

/* Sección Contact */
.contact {
    padding: 80px 0;
    background: white;
}

.contact-content {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 4rem;
    align-items: start;
}

.contact-item {
    display: flex;
    align-items: center;
    gap: 1rem;
    margin-bottom: 2rem;
}

.contact-icon {
    width: 60px;
    height: 60px;
    background: linear-gradient(135deg, #ff6b35, #ffa726);
    border-radius: 50%;
    display: flex;
    align-items: center;
    justify-content: center;
    flex-shrink: 0;
}

.contact-icon i {
    font-size: 1.5rem;
    color: white;
}

.contact-details h4 {
    font-size: 1.2rem;
    font-weight: 600;
    color: #2c3e50;
    margin-bottom: 0.3rem;
}

.contact-details p {
    color: #7f8c8d;
}

.social-links {
    display: flex;
    gap: 1rem;
    margin-top: 2rem;
}

.social-link {
    width: 50px;
    height: 50px;
    background: #f8f9fa;
    border-radius: 50%;
    display: flex;
    align-items: center;
    justify-content: center;
    color: #7f8c8d;
    text-decoration: none;
    transition: all 0.3s ease;
}

.social-link:hover {
    background: linear-gradient(135deg, #ff6b35, #ffa726);
    color: white;
    transform: translateY(-3px);
}

.contact-form {
    background: #f8f9fa;
    padding: 2.5rem;
    border-radius: 15px;
}

.form-group {
    margin-bottom: 1.5rem;
}

.form-group input,
.form-group textarea,
.form-group select {
    width: 100%;
    padding: 1rem;
    border: 2px solid #e9ecef;
    border-radius: 10px;
    font-size: 1rem;
    transition: border-color 0.3s ease;
    background: white;
}

.form-group input:focus,
.form-group textarea:focus,
.form-group select:focus {
    outline: none;
    border-color: #ff6b35;
}

.form-group textarea {
    resize: vertical;
    min-height: 120px;
}

/* Footer */
.footer {
    background: linear-gradient(135deg, #2c3e50, #34495e);
    color: white;
    padding: 3rem 0 1rem;
    position: relative;
    overflow: hidden;
}

.footer-content {
    text-align: center;
    position: relative;
    z-index: 2;
}

.footer-info {
    margin-bottom: 2rem;
}

.footer-logo {
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 0.8rem;
    font-size: 1.8rem;
    font-weight: 700;
    color: #ff6b35;
    margin-bottom: 1rem;
}

.footer-logo i {
    font-size: 2rem;
}

.footer-info p {
    margin-bottom: 1rem;
    opacity: 0.9;
    font-size: 1.1rem;
}

.footer-contact {
    margin-top: 1.5rem;
}

.footer-contact p {
    margin-bottom: 0.5rem;
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 0.5rem;
}

.footer-contact i {
    color: #ff6b35;
}

.footer-paws {
    margin: 2rem 0;
    display: flex;
    justify-content: center;
    gap: 2rem;
    flex-wrap: wrap;
}

.footer-paws i {
    font-size: 2rem;
    color: #ff6b35;
    animation: bounce 2s infinite;
    opacity: 0.8;
}

.footer-paws .paw-1 { animation-delay: 0s; }
.footer-paws .paw-2 { animation-delay: 0.2s; }
.footer-paws .paw-3 { animation-delay: 0.4s; }
.footer-paws .paw-4 { animation-delay: 0.6s; }
.footer-paws .paw-5 { animation-delay: 0.8s; }

@keyframes bounce {
    0%, 20%, 50%, 80%, 100% {
        transform: translateY(0);
    }
    40% {
        transform: translateY(-10px);
    }
    60% {
        transform: translateY(-5px);
    }
}

.footer-bottom {
    border-top: 1px solid rgba(255, 255, 255, 0.1);
    padding-top: 1.5rem;
    margin-top: 1.5rem;
}

.footer-bottom p {
    margin-bottom: 0.5rem;
    opacity: 0.8;
}

.whatsapp {
    background: #25d366 !important;
    color: white !important;
}

.whatsapp:hover {
    background: #128c7e !important;
    transform: translateY(-3px) scale(1.1);
}

/* Notificaciones */
.notification {
    position: fixed;
    top: 20px;
    right: 20px;
    padding: 1rem 1.5rem;
    border-radius: 10px;
    color: white;
    font-weight: 500;
    z-index: 10000;
    transform: translateX(400px);
    transition: transform 0.3s ease;
    max-width: 300px;
    box-shadow: 0 10px 30px rgba(0, 0, 0, 0.2);
}

.notification.success {
    background: linear-gradient(135deg, #27ae60, #2ecc71);
}

.notification.error {
    background: linear-gradient(135deg, #e74c3c, #c0392b);
}

.notification.info {
    background: linear-gradient(135deg, #3498db, #2980b9);
}

.notification.show {
    transform: translateX(0);
}

/* Responsive Design */
@media (max-width: 768px) {
    .nav-menu {
        position: fixed;
        left: -100%;
        top: 70px;
        flex-direction: column;
        background-color: white;
        width: 100%;
        text-align: center;
        transition: 0.3s;
        box-shadow: 0 10px 27px rgba(0, 0, 0, 0.05);
        padding: 2rem 0;
    }

    .nav-menu.active {
        left: 0;
    }

    .nav-toggle {
        display: flex;
    }

    .nav-toggle.active .bar:nth-child(2) {
        opacity: 0;
    }

    .nav-toggle.active .bar:nth-child(1) {
        transform: translateY(8px) rotate(45deg);
    }

    .nav-toggle.active .bar:nth-child(3) {
        transform: translateY(-8px) rotate(-45deg);
    }

    .cart-sidebar {
        width: 100%;
        right: -100%;
    }

    .hero-container {
        grid-template-columns: 1fr;
        text-align: center;
        gap: 2rem;
    }

    .hero-title {
        font-size: 2.5rem;
    }

    .hero-avatar {
        width: 250px;
        height: 250px;
    }

    .about-content {
        grid-template-columns: 1fr;
        gap: 2rem;
    }

    .skills {
        grid-template-columns: repeat(2, 1fr);
    }

    .about-stats {
        flex-direction: row;
        justify-content: space-around;
    }

    .contact-content {
        grid-template-columns: 1fr;
        gap: 2rem;
    }

    .hero-buttons {
        justify-content: center;
    }

    .btn {
        padding: 10px 25px;
        font-size: 0.9rem;
    }
}

@media (max-width: 480px) {
    .hero-title {
        font-size: 2rem;
    }

    .section-title {
        font-size: 2rem;
    }

    .skills {
        grid-template-columns: 1fr;
    }

    .about-stats {
        flex-direction: column;
    }

    .services-grid {
        grid-template-columns: 1fr;
    }

    .portfolio-grid {
        grid-template-columns: 1fr;
    }

    .prices-grid {
        grid-template-columns: 1fr;
    }

    .price-card.featured {
        transform: none;
    }

    .price-card.featured:hover {
        transform: translateY(-10px);
    }

    .additional-grid {
        grid-template-columns: 1fr;
    }

    .footer-paws {
        gap: 1rem;
    }

    .footer-paws i {
        font-size: 1.5rem;
    }

    .amount {
        font-size: 2.5rem;
    }

    .shop-grid {
        grid-template-columns: 1fr;
    }

    .shop-categories {
        gap: 0.5rem;
    }

    .category-filter {
        padding: 0.6rem 1rem;
        font-size: 0.9rem;
    }
}
    </style>
</head>
<body>
    <!-- Overlay del carrito -->
    <div class="cart-overlay" id="cartOverlay"></div>

    <!-- Carrito de compras -->
    <div class="cart-sidebar" id="cartSidebar">
        <div class="cart-header">
            <h3>Mi Carrito</h3>
            <button class="cart-close" id="cartClose">
                <i class="fas fa-times"></i>
            </button>
        </div>
        <div class="cart-items" id="cartItems">
            <div class="cart-empty" id="cartEmpty">
                <i class="fas fa-shopping-cart"></i>
                <p>Tu carrito está vacío</p>
            </div>
        </div>
        <div class="cart-footer" id="cartFooter" style="display: none;">
            <div class="cart-total">
                <span>Total:</span>
                <span class="cart-total-price" id="cartTotal">$0</span>
            </div>
            <button class="cart-checkout" id="cartCheckout">
                <i class="fab fa-whatsapp"></i>
                Finalizar Compra
            </button>
        </div>
    </div>

    <!-- Navegación -->
    <nav class="navbar">
        <div class="nav-container">
            <div class="nav-logo">
                <a href="#home"><i class="fas fa-paw"></i> Huellitas Alegres</a>
            </div>
            <ul class="nav-menu">
                <li class="nav-item">
                    <a href="#home" class="nav-link">Inicio</a>
                </li>
                <li class="nav-item">
                    <a href="#about" class="nav-link">Sobre Nosotros</a>
                </li>
                <li class="nav-item">
                    <a href="#services" class="nav-link">Servicios</a>
                </li>
                <li class="nav-item">
                    <a href="#shop" class="nav-link">Tienda</a>
                </li>
                <li class="nav-item">
                    <a href="#prices" class="nav-link">Precios</a>
                </li>
                <li class="nav-item">
                    <a href="#gallery" class="nav-link">Galería</a>
                </li>
                <li class="nav-item">
                    <a href="#contact" class="nav-link">Contacto</a>
                </li>
                <li class="nav-item">
                    <div class="cart-icon" id="cartIcon">
                        <i class="fas fa-shopping-cart"></i>
                        <span class="cart-count" id="cartCount">0</span>
                    </div>
                </li>
            </ul>
            <div class="nav-toggle" id="mobile-menu">
                <span class="bar"></span>
                <span class="bar"></span>
                <span class="bar"></span>
            </div>
        </div>
    </nav>

    <!-- Sección Hero -->
    <section id="home" class="hero">
        <div class="hero-container">
            <div class="hero-content">
                <h1 class="hero-title">Bienvenido a <span class="highlight">Huellitas Alegres</span></h1>
                <p class="hero-subtitle">Cuidado profesional y amor para tu mejor amigo</p>
                <p class="hero-description">
                    En Huellitas Alegres brindamos servicios especializados para el cuidado de tu mascota.
                    Desde baños y cortes hasta cuidado veterinario, tu perro estará en las mejores manos.
                </p>
                <div class="hero-buttons">
                    <a href="#services" class="btn btn-primary">Nuestros Servicios</a>
                    <a href="#contact" class="btn btn-secondary">Contactar</a>
                </div>
            </div>
            <div class="hero-image">
                <div class="hero-avatar">
                    <img src="https://images.unsplash.com/photo-1552053831-71594a27632d?w=400&h=400&fit=crop&crop=face" 
                         alt="Perro feliz" 
                         onerror="this.style.display='none'; this.nextElementSibling.style.display='flex';">
                    <i class="fas fa-dog fallback-icon" style="display: none;"></i>
                </div>
            </div>
        </div>
    </section>

    <!-- Sección Sobre Nosotros -->
    <section id="about" class="about">
        <div class="container">
            <div class="section-header">
                <h2 class="section-title">Sobre Huellitas Alegres</h2>
                <p class="section-subtitle">Expertos en el cuidado y bienestar de tu mascota</p>
            </div>
            <div class="about-content">
                <div class="about-text">
                    <p>
                        En Huellitas Alegres, ubicados en el hermoso barrio Bocagrande de Cartagena, 
                        nos especializamos en brindar servicios integrales para el cuidado de tu mascota. 
                        Con años de experiencia y amor por los animales, garantizamos el mejor trato para tu compañero.
                    </p>
                    <p>
                        Nuestro equipo está capacitado para ofrecer desde servicios básicos de estética 
                        hasta cuidados especializados. Cada mascota es única y merece atención personalizada, 
                        por eso adaptamos nuestros servicios a las necesidades específicas de tu perro.
                    </p>
                    <div class="skills">
                        <div class="skill-item">
                            <i class="fas fa-heart"></i>
                            <span>Amor</span>
                        </div>
                        <div class="skill-item">
                            <i class="fas fa-cut"></i>
                            <span>Estética</span>
                        </div>
                        <div class="skill-item">
                            <i class="fas fa-shield-alt"></i>
                            <span>Cuidado</span>
                        </div>
                        <div class="skill-item">
                            <i class="fas fa-stethoscope"></i>
                            <span>Salud</span>
                        </div>
                        <div class="skill-item">
                            <i class="fas fa-clock"></i>
                            <span>Puntualidad</span>
                        </div>
                        <div class="skill-item">
                            <i class="fas fa-star"></i>
                            <span>Calidad</span>
                        </div>
                    </div>
                </div>
                <div class="about-stats">
                    <div class="stat-item">
                        <h3>500+</h3>
                        <p>Mascotas Atendidas</p>
                    </div>
                    <div class="stat-item">
                        <h3>5</h3>
                        <p>Años de Experiencia</p>
                    </div>
                    <div class="stat-item">
                        <h3>100%</h3>
                        <p>Clientes Satisfechos</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Sección Servicios -->
    <section id="services" class="services">
        <div class="container">
            <div class="section-header">
                <h2 class="section-title">Nuestros Servicios</h2>
                <p class="section-subtitle">Todo lo que tu mascota necesita en un solo lugar</p>
            </div>
            <div class="services-grid">
                <div class="service-card">
                    <div class="service-icon">
                        <i class="fas fa-shower"></i>
                    </div>
                    <h3>Baño y Secado</h3>
                    <p>Baño completo con productos especializados, secado profesional y desenredado del pelaje.</p>
                </div>
                <div class="service-card">
                    <div class="service-icon">
                        <i class="fas fa-cut"></i>
                    </div>
                    <h3>Corte y Estilismo</h3>
                    <p>Cortes personalizados según la raza y preferencias del dueño. Estilismo profesional.</p>
                </div>
                <div class="service-card">
                    <div class="service-icon">
                        <i class="fas fa-hand-holding-heart"></i>
                    </div>
                    <h3>Cuidado de Uñas</h3>
                    <p>Corte y limado de uñas profesional para mantener la salud y comodidad de tu mascota.</p>
                    </div>
                <div class="service-card">
                    <div class="service-icon">
                        <i class="fas fa-stethoscope"></i>
                    </div>
                    <h3>Consulta Veterinaria</h3>
                    <p>Revisiones generales, vacunación y consultas básicas para mantener la salud de tu perro.</p>
                </div>
                <div class="service-card">
                    <div class="service-icon">
                        <i class="fas fa-home"></i>
                    </div>
                    <h3>Servicio a Domicilio</h3>
                    <p>Llevamos nuestros servicios hasta tu hogar para mayor comodidad de tu mascota.</p>
                </div>
                <div class="service-card">
                    <div class="service-icon">
                        <i class="fas fa-clock"></i>
                    </div>
                    <h3>Cuidado Temporal</h3>
                    <p>Guardería y cuidado temporal para cuando necesites dejar a tu mascota en buenas manos.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Sección Tienda -->
    <section id="shop" class="shop">
        <div class="container">
            <div class="section-header">
                <h2 class="section-title">Tienda de Productos</h2>
                <p class="section-subtitle">Todo lo que tu mascota necesita en un solo lugar</p>
            </div>
            
            <div class="shop-categories">
                <button class="category-filter active" data-category="all">Todos</button>
                <button class="category-filter" data-category="collares">Collares</button>
                <button class="category-filter" data-category="ropa">Ropa</button>
                <button class="category-filter" data-category="comida">Comida</button>
                <button class="category-filter" data-category="juguetes">Juguetes</button>
                <button class="category-filter" data-category="accesorios">Accesorios</button>
                <button class="category-filter" data-category="higiene">Higiene</button>
            </div>
            
            <div class="shop-grid">
                <!-- Collares -->
                <div class="product-card" data-category="collares">
                    <div class="product-image">
                        <img src="https://images.unsplash.com/photo-1601758228041-f3b2795255f1?w=300&h=200&fit=crop" 
                             alt="Collar de Cuero Premium" 
                             onerror="this.style.display='none'; this.nextElementSibling.style.display='flex';">
                        <i class="fas fa-link fallback-icon" style="display: none;"></i>
                        <div class="product-badge">Nuevo</div>
                    </div>
                    <div class="product-info">
                        <div class="product-category">Collares</div>
                        <h3 class="product-name">Collar de Cuero Premium</h3>
                        <p class="product-description">Collar de cuero genuino con hebilla resistente. Disponible en varios tamaños y colores.</p>
                        <div class="product-price">
                            <span class="price-current">$35,000</span>
                            <span class="price-original">$45,000</span>
                        </div>
                        <div class="product-actions">
                            <button class="btn-cart" onclick="addToCart('collar-cuero', 'Collar de Cuero Premium', 35000, 'https://images.unsplash.com/photo-1601758228041-f3b2795255f1?w=300&h=200&fit=crop')">
                                <i class="fas fa-shopping-cart"></i>
                                Agregar
                            </button>
                            <button class="btn-wishlist">
                                <i class="fas fa-heart"></i>
                            </button>
                        </div>
                    </div>
                </div>

                <div class="product-card" data-category="collares">
                    <div class="product-image">
                        <img src="https://images.unsplash.com/photo-1583337130417-3346a1be7dee?w=300&h=200&fit=crop" 
                             alt="Correa Retráctil" 
                             onerror="this.style.display='none'; this.nextElementSibling.style.display='flex';">
                        <i class="fas fa-link fallback-icon" style="display: none;"></i>
                    </div>
                    <div class="product-info">
                        <div class="product-category">Collares</div>
                        <h3 class="product-name">Correa Retráctil</h3>
                        <p class="product-description">Correa retráctil de 5 metros con sistema de frenado automático y mango ergonómico.</p>
                        <div class="product-price">
                            <span class="price-current">$42,000</span>
                        </div>
                        <div class="product-actions">
                            <button class="btn-cart" onclick="addToCart('correa-retractil', 'Correa Retráctil', 42000, 'https://images.unsplash.com/photo-1583337130417-3346a1be7dee?w=300&h=200&fit=crop')">
                                <i class="fas fa-shopping-cart"></i>
                                Agregar
                            </button>
                            <button class="btn-wishlist">
                                <i class="fas fa-heart"></i>
                            </button>
                        </div>
                    </div>
                </div>

                <div class="product-card" data-category="collares">
                    <div class="product-image">
                        <img src="https://images.unsplash.com/photo-1615751072497-5f5169febe17?w=300&h=200&fit=crop" 
                             alt="Collar LED Nocturno" 
                             onerror="this.style.display='none'; this.nextElementSibling.style.display='flex';">
                        <i class="fas fa-lightbulb fallback-icon" style="display: none;"></i>
                        <div class="product-badge">Popular</div>
                    </div>
                    <div class="product-info">
                        <div class="product-category">Collares</div>
                        <h3 class="product-name">Collar LED Nocturno</h3>
                        <p class="product-description">Collar con luces LED recargables para paseos nocturnos. Resistente al agua.</p>
                        <div class="product-price">
                            <span class="price-current">$38,000</span>
                        </div>
                        <div class="product-actions">
                            <button class="btn-cart" onclick="addToCart('collar-led', 'Collar LED Nocturno', 38000, 'https://images.unsplash.com/photo-1615751072497-5f5169febe17?w=300&h=200&fit=crop')">
                                <i class="fas fa-shopping-cart"></i>
                                Agregar
                            </button>
                            <button class="btn-wishlist">
                                <i class="fas fa-heart"></i>
                            </button>
                        </div>
                    </div>
                </div>
                
                <!-- Ropa -->
                <div class="product-card" data-category="ropa">
                    <div class="product-image">
                        <img src="https://images.unsplash.com/photo-1544568100-847a948585b9?w=300&h=200&fit=crop" 
                             alt="Suéter Abrigado" 
                             onerror="this.style.display='none'; this.nextElementSibling.style.display='flex';">
                        <i class="fas fa-tshirt fallback-icon" style="display: none;"></i>
                    </div>
                    <div class="product-info">
                        <div class="product-category">Ropa</div>
                        <h3 class="product-name">Suéter Abrigado</h3>
                        <p class="product-description">Suéter cómodo y cálido para los días fríos. Material suave y transpirable.</p>
                        <div class="product-price">
                            <span class="price-current">$28,000</span>
                        </div>
                        <div class="product-actions">
                            <button class="btn-cart" onclick="addToCart('sueter-abrigado', 'Suéter Abrigado', 28000, 'https://images.unsplash.com/photo-1544568100-847a948585b9?w=300&h=200&fit=crop')">
                                <i class="fas fa-shopping-cart"></i>
                                Agregar
                            </button>
                            <button class="btn-wishlist">
                                <i class="fas fa-heart"></i>
                            </button>
                        </div>
                    </div>
                </div>

                <div class="product-card" data-category="ropa">
                    <div class="product-image">
                        <img src="https://images.unsplash.com/photo-1601758003122-53c40e686a19?w=300&h=200&fit=crop" 
                             alt="Impermeable" 
                             onerror="this.style.display='none'; this.nextElementSibling.style.display='flex';">
                        <i class="fas fa-umbrella fallback-icon" style="display: none;"></i>
                        <div class="product-badge">Nuevo</div>
                    </div>
                    <div class="product-info">
                        <div class="product-category">Ropa</div>
                        <h3 class="product-name">Impermeable</h3>
                        <p class="product-description">Impermeable resistente con capucha para días lluviosos. Fácil de poner y quitar.</p>
                        <div class="product-price">
                            <span class="price-current">$32,000</span>
                        </div>
                        <div class="product-actions">
                            <button class="btn-cart" onclick="addToCart('impermeable', 'Impermeable', 32000, 'https://images.unsplash.com/photo-1601758003122-53c40e686a19?w=300&h=200&fit=crop')">
                                <i class="fas fa-shopping-cart"></i>
                                Agregar
                            </button>
                            <button class="btn-wishlist">
                                <i class="fas fa-heart"></i>
                            </button>
                        </div>
                    </div>
                </div>

                <div class="product-card" data-category="ropa">
                    <div class="product-image">
                        <img src="https://images.unsplash.com/photo-1587300003388-59208cc962cb?w=300&h=200&fit=crop" 
                             alt="Chaleco Reflectivo" 
                             onerror="this.style.display='none'; this.nextElementSibling.style.display='flex';">
                        <i class="fas fa-vest fallback-icon" style="display: none;"></i>
                    </div>
                    <div class="product-info">
                        <div class="product-category">Ropa</div>
                        <h3 class="product-name">Chaleco Reflectivo</h3>
                        <p class="product-description">Chaleco de seguridad con bandas reflectivas para mayor visibilidad nocturna.</p>
                        <div class="product-price">
                            <span class="price-current">$25,000</span>
                        </div>
                        <div class="product-actions">
                            <button class="btn-cart" onclick="addToCart('chaleco-reflectivo', 'Chaleco Reflectivo', 25000, 'https://images.unsplash.com/photo-1587300003388-59208cc962cb?w=300&h=200&fit=crop')">
                                <i class="fas fa-shopping-cart"></i>
                                Agregar
                            </button>
                            <button class="btn-wishlist">
                                <i class="fas fa-heart"></i>
                            </button>
                        </div>
                    </div>
                </div>
                
                <!-- Comida -->
                <div class="product-card" data-category="comida">
                    <div class="product-image">
                        <img src="https://images.unsplash.com/photo-1589924691995-400dc9ecc119?w=300&h=200&fit=crop" 
                             alt="Alimento Premium" 
                             onerror="this.style.display='none'; this.nextElementSibling.style.display='flex';">
                        <i class="fas fa-bone fallback-icon" style="display: none;"></i>
                        <div class="product-badge">Bestseller</div>
                    </div>
                    <div class="product-info">
                        <div class="product-category">Comida</div>
                        <h3 class="product-name">Alimento Premium (15kg)</h3>
                        <p class="product-description">Alimento balanceado de alta calidad con proteínas naturales y vitaminas esenciales.</p>
                        <div class="product-price">
                            <span class="price-current">$85,000</span>
                            <span class="price-original">$95,000</span>
                        </div>
                        <div class="product-actions">
                            <button class="btn-cart" onclick="addToCart('alimento-premium', 'Alimento Premium (15kg)', 85000, 'https://images.unsplash.com/photo-1589924691995-400dc9ecc119?w=300&h=200&fit=crop')">
                                <i class="fas fa-shopping-cart"></i>
                                Agregar
                            </button>
                            <button class="btn-wishlist">
                                <i class="fas fa-heart"></i>
                            </button>
                        </div>
                    </div>
                </div>

                <div class="product-card" data-category="comida">
                    <div class="product-image">
                        <img src="https://images.unsplash.com/photo-1605568427561-40dd23c2acea?w=300&h=200&fit=crop" 
                             alt="Snacks Naturales" 
                             onerror="this.style.display='none'; this.nextElementSibling.style.display='flex';">
                        <i class="fas fa-cookie-bite fallback-icon" style="display: none;"></i>
                    </div>
                    <div class="product-info">
                        <div class="product-category">Comida</div>
                        <h3 class="product-name">Snacks Naturales</h3>
                        <p class="product-description">Premios naturales sin conservantes artificiales. Perfectos para entrenamiento.</p>
                        <div class="product-price">
                            <span class="price-current">$15,000</span>
                        </div>
                        <div class="product-actions">
                            <button class="btn-cart" onclick="addToCart('snacks-naturales', 'Snacks Naturales', 15000, 'https://images.unsplash.com/photo-1605568427561-40dd23c2acea?w=300&h=200&fit=crop')">
                                <i class="fas fa-shopping-cart"></i>
                                Agregar
                            </button>
                            <button class="btn-wishlist">
                                <i class="fas fa-heart"></i>
                            </button>
                        </div>
                    </div>
                </div>

                <div class="product-card" data-category="comida">
                    <div class="product-image">
                        <img src="https://images.unsplash.com/photo-1628009368231-7bb7cfcb0def?w=300&h=200&fit=crop" 
                             alt="Comida Húmeda" 
                             onerror="this.style.display='none'; this.nextElementSibling.style.display='flex';">
                        <i class="fas fa-can-food fallback-icon" style="display: none;"></i>
                        <div class="product-badge">Oferta</div>
                    </div>
                    <div class="product-info">
                        <div class="product-category">Comida</div>
                        <h3 class="product-name">Comida Húmeda (Pack 12)</h3>
                        <p class="product-description">Pack de 12 latas de comida húmeda con diferentes sabores. Rica en proteínas.</p>
                        <div class="product-price">
                            <span class="price-current">$48,000</span>
                            <span class="price-original">$60,000</span>
                        </div>
                        <div class="product-actions">
                            <button class="btn-cart" onclick="addToCart('comida-humeda', 'Comida Húmeda (Pack 12)', 48000, 'https://images.unsplash.com/photo-1628009368231-7bb7cfcb0def?w=300&h=200&fit=crop')">
                                <i class="fas fa-shopping-cart"></i>
                                Agregar
                            </button>
                            <button class="btn-wishlist">
                                <i class="fas fa-heart"></i>
                            </button>
                        </div>
                    </div>
                </div>
                
                <!-- Juguetes -->
                <div class="product-card" data-category="juguetes">
                    <div class="product-image">
                        <img src="https://images.unsplash.com/photo-1601758125946-6ec2ef64daf8?w=300&h=200&fit=crop" 
                             alt="Pelota Interactiva" 
                             onerror="this.style.display='none'; this.nextElementSibling.style.display='flex';">
                        <i class="fas fa-baseball-ball fallback-icon" style="display: none;"></i>
                    </div>
                    <div class="product-info">
                        <div class="product-category">Juguetes</div>
                        <h3 class="product-name">Pelota Interactiva</h3>
                        <p class="product-description">Pelota resistente con sonido que mantiene a tu perro entretenido y activo.</p>
                        <div class="product-price">
                            <span class="price-current">$18,000</span>
                        </div>
                        <div class="product-actions">
                            <button class="btn-cart" onclick="addToCart('pelota-interactiva', 'Pelota Interactiva', 18000, 'https://images.unsplash.com/photo-1601758125946-6ec2ef64daf8?w=300&h=200&fit=crop')">
                                <i class="fas fa-shopping-cart"></i>
                                Agregar
                            </button>
                            <button class="btn-wishlist">
                                <i class="fas fa-heart"></i>
                            </button>
                        </div>
                    </div>
                </div>

                <div class="product-card" data-category="juguetes">
                    <div class="product-image">
                        <img src="https://images.unsplash.com/photo-1605568427561-40dd23c2acea?w=300&h=200&fit=crop" 
                             alt="Cuerda de Juego" 
                             onerror="this.style.display='none'; this.nextElementSibling.style.display='flex';">
                        <i class="fas fa-rope fallback-icon" style="display: none;"></i>
                    </div>
                    <div class="product-info">
                        <div class="product-category">Juguetes</div>
                        <h3 class="product-name">Cuerda de Juego</h3>
                        <p class="product-description">Cuerda resistente de algodón natural para juegos de tirar y limpiar dientes.</p>
                        <div class="product-price">
                            <span class="price-current">$12,000</span>
                        </div>
                        <div class="product-actions">
                            <button class="btn-cart" onclick="addToCart('cuerda-juego', 'Cuerda de Juego', 12000, 'https://images.unsplash.com/photo-1605568427561-40dd23c2acea?w=300&h=200&fit=crop')">
                                <i class="fas fa-shopping-cart"></i>
                                Agregar
                            </button>
                            <button class="btn-wishlist">
                                <i class="fas fa-heart"></i>
                            </button>
                        </div>
                    </div>
                </div>

                <div class="product-card" data-category="juguetes">
                    <div class="product-image">
                        <img src="https://images.unsplash.com/photo-1601758228041-f3b2795255f1?w=300&h=200&fit=crop" 
                             alt="Kong Rellenable" 
                             onerror="this.style.display='none'; this.nextElementSibling.style.display='flex';">
                        <i class="fas fa-bone fallback-icon" style="display: none;"></i>
                        <div class="product-badge">Popular</div>
                    </div>
                    <div class="product-info">
                        <div class="product-category">Juguetes</div>
                        <h3 class="product-name">Kong Rellenable</h3>
                        <p class="product-description">Juguete resistente que se puede rellenar con premios para mantener entretenido a tu perro.</p>
                        <div class="product-price">
                            <span class="price-current">$22,000</span>
                        </div>
                        <div class="product-actions">
                            <button class="btn-cart" onclick="addToCart('kong-rellenable', 'Kong Rellenable', 22000, 'https://images.unsplash.com/photo-1601758228041-f3b2795255f1?w=300&h=200&fit=crop')">
                                <i class="fas fa-shopping-cart"></i>
                                Agregar
                            </button>
                            <button class="btn-wishlist">
                                <i class="fas fa-heart"></i>
                            </button>
                        </div>
                    </div>
                </div>
                
                <!-- Accesorios -->
                <div class="product-card" data-category="accesorios">
                    <div class="product-image">
                        <img src="https://images.unsplash.com/photo-1601758003122-53c40e686a19?w=300&h=200&fit=crop" 
                             alt="Cama Ortopédica" 
                             onerror="this.style.display='none'; this.nextElementSibling.style.display='flex';">
                        <i class="fas fa-bed fallback-icon" style="display: none;"></i>
                        <div class="product-badge">Oferta</div>
                    </div>
                    <div class="product-info">
                        <div class="product-category">Accesorios</div>
                        <h3 class="product-name">Cama Ortopédica</h3>
                        <p class="product-description">Cama cómoda con soporte ortopédico para el descanso perfecto de tu mascota.</p>
                        <div class="product-price">
                            <span class="price-current">$65,000</span>
                            <span class="price-original">$80,000</span>
                        </div>
                        <div class="product-actions">
                            <button class="btn-cart" onclick="addToCart('cama-ortopedica', 'Cama Ortopédica', 65000, 'https://images.unsplash.com/photo-1601758003122-53c40e686a19?w=300&h=200&fit=crop')">
                                <i class="fas fa-shopping-cart"></i>
                                Agregar
                            </button>
                            <button class="btn-wishlist">
                                <i class="fas fa-heart"></i>
                            </button>
                        </div>
                    </div>
                </div>

                <div class="product-card" data-category="accesorios">
                    <div class="product-image">
                        <img src="https://images.unsplash.com/photo-1583337130417-3346a1be7dee?w=300&h=200&fit=crop" 
                             alt="Comedero Automático" 
                             onerror="this.style.display='none'; this.nextElementSibling.style.display='flex';">
                        <i class="fas fa-robot fallback-icon" style="display: none;"></i>
                        <div class="product-badge">Nuevo</div>
                    </div>
                    <div class="product-info">
                        <div class="product-category">Accesorios</div>
                        <h3 class="product-name">Comedero Automático</h3>
                        <p class="product-description">Dispensador automático de comida con temporizador. Perfecto para horarios regulares.</p>
                        <div class="product-price">
                            <span class="price-current">$95,000</span>
                        </div>
                        <div class="product-actions">
                            <button class="btn-cart" onclick="addToCart('comedero-automatico', 'Comedero Automático', 95000, 'https://images.unsplash.com/photo-1583337130417-3346a1be7dee?w=300&h=200&fit=crop')">
                                <i class="fas fa-shopping-cart"></i>
                                Agregar
                            </button>
                            <button class="btn-wishlist">
                                <i class="fas fa-heart"></i>
                            </button>
                        </div>
                    </div>
                </div>

                <div class="product-card" data-category="accesorios">
                    <div class="product-image">
                        <img src="https://images.unsplash.com/photo-1615751072497-5f5169febe17?w=300&h=200&fit=crop" 
                             alt="Transportadora" 
                             onerror="this.style.display='none'; this.nextElementSibling.style.display='flex';">
                        <i class="fas fa-suitcase fallback-icon" style="display: none;"></i>
                    </div>
                    <div class="product-info">
                        <div class="product-category">Accesorios</div>
                        <h3 class="product-name">Transportadora</h3>
                        <p class="product-description">Transportadora resistente y cómoda para viajes. Aprobada para vuelos comerciales.</p>
                        <div class="product-price">
                            <span class="price-current">$75,000</span>
                        </div>
                        <div class="product-actions">
                            <button class="btn-cart" onclick="addToCart('transportadora', 'Transportadora', 75000, 'https://images.unsplash.com/photo-1615751072497-5f5169febe17?w=300&h=200&fit=crop')">
                                <i class="fas fa-shopping-cart"></i>
                                Agregar
                            </button>
                            <button class="btn-wishlist">
                                <i class="fas fa-heart"></i>
                            </button>
                        </div>
                    </div>
                </div>

                <!-- Higiene -->
                <div class="product-card" data-category="higiene">
                    <div class="product-image">
                        <img src="https://images.unsplash.com/photo-1544568100-847a948585b9?w=300&h=200&fit=crop" 
                             alt="Shampoo Especializado" 
                             onerror="this.style.display='none'; this.nextElementSibling.style.display='flex';">
                        <i class="fas fa-pump-soap fallback-icon" style="display: none;"></i>
                        <div class="product-badge">Popular</div>
                    </div>
                    <div class="product-info">
                        <div class="product-category">Higiene</div>
                        <h3 class="product-name">Shampoo Especializado</h3>
                        <p class="product-description">Shampoo hipoalergénico con ingredientes naturales. Ideal para pieles sensibles.</p>
                        <div class="product-price">
                            <span class="price-current">$24,000</span>
                        </div>
                        <div class="product-actions">
                            <button class="btn-cart" onclick="addToCart('shampoo-especializado', 'Shampoo Especializado', 24000, 'https://images.unsplash.com/photo-1544568100-847a948585b9?w=300&h=200&fit=crop')">
                                <i class="fas fa-shopping-cart"></i>
                                Agregar
                            </button>
                            <button class="btn-wishlist">
                                <i class="fas fa-heart"></i>
                            </button>
                        </div>
                    </div>
                </div>

                <div class="product-card" data-category="higiene">
                    <div class="product-image">
                        <img src="https://images.unsplash.com/photo-1587300003388-59208cc962cb?w=300&h=200&fit=crop" 
                             alt="Kit Dental Completo" 
                             onerror="this.style.display='none'; this.nextElementSibling.style.display='flex';">
                        <i class="fas fa-tooth fallback-icon" style="display: none;"></i>
                    </div>
                    <div class="product-info">
                        <div class="product-category">Higiene</div>
                        <h3 class="product-name">Kit Dental Completo</h3>
                        <p class="product-description">Kit con cepillo, pasta dental y enjuague bucal especial para perros.</p>
                        <div class="product-price">
                            <span class="price-current">$19,000</span>
                        </div>
                        <div class="product-actions">
                            <button class="btn-cart" onclick="addToCart('kit-dental', 'Kit Dental Completo', 19000, 'https://images.unsplash.com/photo-1587300003388-59208cc962cb?w=300&h=200&fit=crop')">
                                <i class="fas fa-shopping-cart"></i>
                                Agregar
                            </button>
                            <button class="btn-wishlist">
                                <i class="fas fa-heart"></i>
                            </button>
                        </div>
                    </div>
                </div>

                <div class="product-card" data-category="higiene">
                    <div class="product-image">
                        <img src="https://images.unsplash.com/photo-1601758228041-f3b2795255f1?w=300&h=200&fit=crop" 
                             alt="Toallitas Húmedas" 
                             onerror="this.style.display='none'; this.nextElementSibling.style.display='flex';">
                        <i class="fas fa-tissue fallback-icon" style="display: none;"></i>
                    </div>
                    <div class="product-info">
                        <div class="product-category">Higiene</div>
                        <h3 class="product-name">Toallitas Húmedas</h3>
                        <p class="product-description">Toallitas húmedas antibacteriales para limpieza rápida de patas y pelaje.</p>
                        <div class="product-price">
                            <span class="price-current">$8,000</span>
                        </div>
                        <div class="product-actions">
                            <button class="btn-cart" onclick="addToCart('toallitas-humedas', 'Toallitas Húmedas', 8000, 'https://images.unsplash.com/photo-1601758228041-f3b2795255f1?w=300&h=200&fit=crop')">
                                <i class="fas fa-shopping-cart"></i>
                                Agregar
                            </button>
                            <button class="btn-wishlist">
                                <i class="fas fa-heart"></i>
                            </button>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Sección Precios -->
    <section id="prices" class="prices">
        <div class="container">
            <div class="section-header">
                <h2 class="section-title">Nuestros Precios</h2>
                <p class="section-subtitle">Servicios de calidad a precios justos</p>
            </div>
            <div class="prices-grid">
                <div class="price-card">
                    <div class="price-header">
                        <h3>Básico</h3>
                        <div class="price">
                            <span class="currency">$</span>
                            <span class="amount">25,000</span>
                        </div>
                        <p class="price-description">Perfecto para el cuidado esencial</p>
                    </div>
                    <ul class="price-features">
                        <li><i class="fas fa-check"></i> Baño completo</li>
                        <li><i class="fas fa-check"></i> Secado profesional</li>
                        <li><i class="fas fa-check"></i> Desenredado básico</li>
                        <li><i class="fas fa-check"></i> Limpieza de oídos</li>
                    </ul>
                    <a href="#contact" class="btn btn-outline">Reservar</a>
                </div>
                
                <div class="price-card featured">
                    <div class="price-badge">Más Popular</div>
                    <div class="price-header">
                        <h3>Completo</h3>
                        <div class="price">
                            <span class="currency">$</span>
                            <span class="amount">45,000</span>
                        </div>
                        <p class="price-description">El paquete más solicitado</p>
                    </div>
                    <ul class="price-features">
                        <li><i class="fas fa-check"></i> Todo del paquete básico</li>
                        <li><i class="fas fa-check"></i> Corte personalizado</li>
                        <li><i class="fas fa-check"></i> Corte de uñas</li>
                        <li><i class="fas fa-check"></i> Limpieza dental básica</li>
                        <li><i class="fas fa-check"></i> Perfume para mascotas</li>
                    </ul>
                    <a href="#contact" class="btn btn-primary">Reservar</a>
                </div>
                
                <div class="price-card">
                    <div class="price-header">
                        <h3>Premium</h3>
                        <div class="price">
                            <span class="currency">$</span>
                            <span class="amount">65,000</span>
                        </div>
                        <p class="price-description">Experiencia de lujo total</p>
                    </div>
                    <ul class="price-features">
                        <li><i class="fas fa-check"></i> Todo del paquete completo</li>
                        <li><i class="fas fa-check"></i> Tratamiento de spa</li>
                        <li><i class="fas fa-check"></i> Masaje relajante</li>
                        <li><i class="fas fa-check"></i> Consulta veterinaria</li>
                        <li><i class="fas fa-check"></i> Sesión de fotos</li>
                    </ul>
                    <a href="#contact" class="btn btn-outline">Reservar</a>
                </div>
            </div>
            
            <div class="additional-services">
                <h3>Servicios Adicionales</h3>
                <div class="additional-grid">
                    <div class="additional-item">
                        <span class="service-name">Servicio a Domicilio</span>
                        <span class="service-price">+$10,000</span>
                    </div>
                    <div class="additional-item">
                        <span class="service-name">Cuidado Temporal (por día)</span>
                        <span class="service-price">$20,000</span>
                    </div>
                    <div class="additional-item">
                        <span class="service-name">Consulta Veterinaria</span>
                        <span class="service-price">$35,000</span>
                    </div>
                    <div class="additional-item">
                        <span class="service-name">Vacunación</span>
                        <span class="service-price">$25,000</span>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Sección Galería -->
    <section id="gallery" class="portfolio">
        <div class="container">
            <div class="section-header">
                <h2 class="section-title">Galería de Nuestros Clientes</h2>
                <p class="section-subtitle">Mascotas felices y bien cuidadas</p>
            </div>
            <div class="portfolio-grid">
                <div class="portfolio-item">
                    <div class="portfolio-image">
                        <img src="https://images.unsplash.com/photo-1552053831-71594a27632d?w=400&h=300&fit=crop" 
                             alt="Max - Golden Retriever" 
                             onerror="this.style.display='none'; this.nextElementSibling.style.display='flex';">
                        <i class="fas fa-dog fallback-icon" style="display: none;"></i>
                        <div class="portfolio-overlay">
                            <div class="portfolio-info">
                                <h4>Max - Golden Retriever</h4>
                                <p>Después de su sesión de spa completa</p>
                            </div>
                        </div>
                    </div>
                </div>
                <div class="portfolio-item">
                    <div class="portfolio-image">
                        <img src="https://images.unsplash.com/photo-1583337130417-3346a1be7dee?w=400&h=300&fit=crop" 
                             alt="Luna - Poodle" 
                             onerror="this.style.display='none'; this.nextElementSibling.style.display='flex';">
                        <i class="fas fa-dog fallback-icon" style="display: none;"></i>
                        <div class="portfolio-overlay">
                            <div class="portfolio-info">
                                <h4>Luna - Poodle</h4>
                                <p>Corte estilizado y adorable</p>
                            </div>
                        </div>
                    </div>
                </div>
                <div class="portfolio-item">
                    <div class="portfolio-image">
                        <img src="https://images.unsplash.com/photo-1601758228041-f3b2795255f1?w=400&h=300&fit=crop" 
                             alt="Rocky - Pastor Alemán" 
                             onerror="this.style.display='none'; this.nextElementSibling.style.display='flex';">
                        <i class="fas fa-dog fallback-icon" style="display: none;"></i>
                        <div class="portfolio-overlay">
                            <div class="portfolio-info">
                                <h4>Rocky - Pastor Alemán</h4>
                                <p>Feliz después de su cuidado</p>
                            </div>
                        </div>
                    </div>
                </div>
                <div class="portfolio-item">
                    <div class="portfolio-image">
                        <img src="https://images.unsplash.com/photo-1544568100-847a948585b9?w=400&h=300&fit=crop" 
                             alt="Bella - Labrador" 
                             onerror="this.style.display='none'; this.nextElementSibling.style.display='flex';">
                        <i class="fas fa-dog fallback-icon" style="display: none;"></i>
                        <div class="portfolio-overlay">
                            <div class="portfolio-info">
                                <h4>Bella - Labrador</h4>
                                <p>Relajada después del masaje</p>
                            </div>
                        </div>
                    </div>
                </div>
                <div class="portfolio-item">
                    <div class="portfolio-image">
                        <img src="https://images.unsplash.com/photo-1587300003388-59208cc962cb?w=400&h=300&fit=crop" 
                             alt="Charlie - Bulldog" 
                             onerror="this.style.display='none'; this.nextElementSibling.style.display='flex';">
                        <i class="fas fa-dog fallback-icon" style="display: none;"></i>
                        <div class="portfolio-overlay">
                            <div class="portfolio-info">
                                <h4>Charlie - Bulldog</h4>
                                <p>Luciendo su nuevo corte</p>
                            </div>
                        </div>
                    </div>
                </div>
                <div class="portfolio-item">
                    <div class="portfolio-image">
                        <img src="https://images.unsplash.com/photo-1615751072497-5f5169febe17?w=400&h=300&fit=crop" 
                             alt="Mia - Chihuahua" 
                             onerror="this.style.display='none'; this.nextElementSibling.style.display='flex';">
                        <i class="fas fa-dog fallback-icon" style="display: none;"></i>
                        <div class="portfolio-overlay">
                            <div class="portfolio-info">
                                <h4>Mia - Chihuahua</h4>
                                <p>Pequeña pero con gran estilo</p>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Sección Contacto -->
    <section id="contact" class="contact">
        <div class="container">
            <div class="section-header">
                <h2 class="section-title">Contacto</h2>
                <p class="section-subtitle">¡Agenda una cita para tu mascota!</p>
            </div>
            <div class="contact-content">
                <div class="contact-info">
                    <div class="contact-item">
                        <div class="contact-icon">
                            <i class="fas fa-user"></i>
                        </div>
                        <div class="contact-details">
                            <h4>Propietario</h4>
                            <p>Dewin Luna</p>
                        </div>
                    </div>
                    <div class="contact-item">
                        <div class="contact-icon">
                            <i class="fas fa-phone"></i>
                        </div>
                        <div class="contact-details">
                            <h4>Teléfono / WhatsApp</h4>
                            <p>310 411 9101</p>
                        </div>
                    </div>
                    <div class="contact-item">
                        <div class="contact-icon">
                            <i class="fas fa-map-marker-alt"></i>
                        </div>
                        <div class="contact-details">
                            <h4>Ubicación</h4>
                            <p>Bocagrande, Cartagena</p>
                        </div>
                    </div>
                    <div class="contact-item">
                        <div class="contact-icon">
                            <i class="fas fa-clock"></i>
                        </div>
                        <div class="contact-details">
                            <h4>Horarios</h4>
                            <p>Lun - Sáb: 8:00 AM - 6:00 PM</p>
                        </div>
                    </div>
                    <div class="social-links">
                        <a href="https://wa.me/573104119101" class="social-link whatsapp" target="_blank">
                            <i class="fab fa-whatsapp"></i>
                        </a>
                        <a href="#" class="social-link"><i class="fab fa-facebook"></i></a>
                        <a href="#" class="social-link"><i class="fab fa-instagram"></i></a>
                    </div>
                </div>
                <form class="contact-form">
                    <div class="form-group">
                        <input type="text" id="name" name="name" placeholder="Tu nombre" required>
                    </div>
                    <div class="form-group">
                        <input type="tel" id="phone" name="phone" placeholder="Tu teléfono" required>
                    </div>
                    <div class="form-group">
                        <input type="text" id="pet-name" name="pet-name" placeholder="Nombre de tu mascota" required>
                    </div>
                    <div class="form-group">
                        <select id="service" name="service" required>
                            <option value="">Selecciona un servicio</option>
                            <option value="basico">Paquete Básico - $25,000</option>
                            <option value="completo">Paquete Completo - $45,000</option>
                            <option value="premium">Paquete Premium - $65,000</option>
                            <option value="domicilio">Servicio a Domicilio</option>
                            <option value="veterinaria">Consulta Veterinaria</option>
                            <option value="productos">Productos de la Tienda</option>
                        </select>
                    </div>
                    <div class="form-group">
                        <textarea id="message" name="message" placeholder="Cuéntanos sobre tu mascota y cuándo te gustaría agendar" rows="4" required></textarea>
                    </div>
                    <button type="submit" class="btn btn-primary">Enviar Solicitud</button>
                </form>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="footer">
        <div class="container">
            <div class="footer-content">
                <div class="footer-info">
                    <div class="footer-logo">
                        <i class="fas fa-paw"></i>
                        <span>Huellitas Alegres</span>
                    </div>
                    <p>Cuidado profesional y amor para tu mejor amigo</p>
                    <div class="footer-contact">
                        <p><strong>Dewin Luna</strong></p>
                        <p><i class="fas fa-phone"></i> 310 411 9101</p>
                        <p><i class="fas fa-map-marker-alt"></i> Bocagrande, Cartagena</p>
                    </div>
                </div>
                <div class="footer-paws">
                    <i class="fas fa-paw paw-1"></i>
                    <i class="fas fa-paw paw-2"></i>
                    <i class="fas fa-paw paw-3"></i>
                    <i class="fas fa-paw paw-4"></i>
                    <i class="fas fa-paw paw-5"></i>
                </div>
                <div class="footer-bottom">
                    <p>&copy; 2024 Huellitas Alegres. Todos los derechos reservados.</p>
                    <p>Hecho con ❤️ para los amantes de las mascotas</p>
                </div>
            </div>
        </div>
    </footer>

    <script>
// Variables globales del carrito
let cart = [];
let cartItemCount = 0;

// Navegación móvil
const mobileMenu = document.getElementById('mobile-menu');
const navMenu = document.querySelector('.nav-menu');

mobileMenu.addEventListener('click', () => {
    mobileMenu.classList.toggle('active');
    navMenu.classList.toggle('active');
});

// Cerrar menú móvil al hacer clic en un enlace
document.querySelectorAll('.nav-link').forEach(link => {
    link.addEventListener('click', () => {
        mobileMenu.classList.remove('active');
        navMenu.classList.remove('active');
    });
});

// Navegación suave
document.querySelectorAll('a[href^="#"]').forEach(anchor => {
    anchor.addEventListener('click', function (e) {
        e.preventDefault();
        const target = document.querySelector(this.getAttribute('href'));
        if (target) {
            target.scrollIntoView({
                behavior: 'smooth',
                block: 'start'
            });
        }
    });
});

// Cambiar estilo de navegación al hacer scroll
window.addEventListener('scroll', () => {
    const navbar = document.querySelector('.navbar');
    if (window.scrollY > 100) {
        navbar.style.background = 'rgba(255, 255, 255, 0.98)';
        navbar.style.boxShadow = '0 2px 20px rgba(0, 0, 0, 0.15)';
    } else {
        navbar.style.background = 'rgba(255, 255, 255, 0.95)';
        navbar.style.boxShadow = '0 2px 20px rgba(0, 0, 0, 0.1)';
    }
});

// Filtros de la tienda
document.addEventListener('DOMContentLoaded', () => {
    const categoryFilters = document.querySelectorAll('.category-filter');
    const productCards = document.querySelectorAll('.product-card');

    categoryFilters.forEach(filter => {
        filter.addEventListener('click', () => {
            // Remover clase active de todos los filtros
            categoryFilters.forEach(f => f.classList.remove('active'));
            // Agregar clase active al filtro clickeado
            filter.classList.add('active');

            const category = filter.getAttribute('data-category');

            productCards.forEach(card => {
                if (category === 'all' || card.getAttribute('data-category') === category) {
                    card.style.display = 'block';
                    card.style.animation = 'fadeIn 0.5s ease';
                } else {
                    card.style.display = 'none';
                }
            });
        });
    });
});

// Funciones del carrito de compras - COMPLETAMENTE ARREGLADO
function addToCart(id, name, price, imageUrl) {
    console.log('=== AGREGANDO AL CARRITO ===');
    console.log('ID:', id, 'Nombre:', name, 'Precio:', price);
    
    // Buscar si el producto ya existe en el carrito
    let existingItemIndex = -1;
    for (let i = 0; i < cart.length; i++) {
        if (cart[i].id === id) {
            existingItemIndex = i;
            break;
        }
    }
    
    if (existingItemIndex !== -1) {
        // Si existe, aumentar cantidad
        cart[existingItemIndex].quantity += 1;
        console.log('Producto existente actualizado:', cart[existingItemIndex]);
    } else {
        // Si no existe, agregar nuevo producto
        const newItem = {
            id: id,
            name: name,
            price: parseInt(price),
            image: imageUrl,
            quantity: 1
        };
        cart.push(newItem);
        console.log('Nuevo producto agregado:', newItem);
    }
    
    // Actualizar contador total
    cartItemCount = 0;
    for (let i = 0; i < cart.length; i++) {
        cartItemCount += cart[i].quantity;
    }
    
    console.log('Carrito completo:', cart);
    console.log('Total items:', cartItemCount);
    console.log('=== FIN AGREGAR ===');
    
    updateCartUI();
    showNotification(`${name} agregado al carrito`, 'success');
}

function removeFromCart(id) {
    console.log('=== ELIMINANDO DEL CARRITO ===');
    console.log('Eliminando ID:', id);
    
    // Filtrar el carrito para remover el item
    const newCart = [];
    for (let i = 0; i < cart.length; i++) {
        if (cart[i].id !== id) {
            newCart.push(cart[i]);
        }
    }
    cart = newCart;
    
    console.log('Carrito después de eliminar:', cart);
    console.log('=== FIN ELIMINAR ===');
    
    updateCartUI();
    showNotification('Producto eliminado del carrito', 'info');
}

function updateQuantity(id, change) {
    console.log('=== ACTUALIZANDO CANTIDAD ===');
    console.log('ID:', id, 'Cambio:', change);
    
    // Buscar el item en el carrito
    for (let i = 0; i < cart.length; i++) {
        if (cart[i].id === id) {
            cart[i].quantity += change;
            console.log('Nueva cantidad:', cart[i].quantity);
            
            if (cart[i].quantity <= 0) {
                console.log('Cantidad 0 o menor, eliminando producto');
                removeFromCart(id);
                return;
            } else {
                updateCartUI();
                return;
            }
        }
    }
    
    console.log('=== FIN ACTUALIZAR CANTIDAD ===');
}

function updateCartUI() {
    console.log('=== ACTUALIZANDO UI DEL CARRITO ===');
    
    const cartCount = document.getElementById('cartCount');
    const cartItems = document.getElementById('cartItems');
    const cartFooter = document.getElementById('cartFooter');
    const cartTotal = document.getElementById('cartTotal');
    
    // Recalcular totales
    let totalItems = 0;
    let totalPrice = 0;
    
    for (let i = 0; i < cart.length; i++) {
        totalItems += cart[i].quantity;
        totalPrice += (cart[i].price * cart[i].quantity);
    }
    
    console.log('Total productos únicos:', cart.length);
    console.log('Total items (con cantidades):', totalItems);
    console.log('Precio total:', totalPrice);
    
    // Actualizar contador del carrito
    if (totalItems > 0) {
        cartCount.textContent = totalItems;
        cartCount.style.display = 'flex';
    } else {
        cartCount.style.display = 'none';
    }
    
    // Actualizar contenido del carrito
    if (cart.length === 0) {
        cartItems.innerHTML = '<div class="cart-empty"><i class="fas fa-shopping-cart"></i><p>Tu carrito está vacío</p></div>';
        cartFooter.style.display = 'none';
    } else {
        cartFooter.style.display = 'block';
        
        // Generar HTML manualmente para evitar problemas
        let cartHTML = '';
        for (let i = 0; i < cart.length; i++) {
            const item = cart[i];
            cartHTML += `
                <div class="cart-item">
                    <div class="cart-item-image">
                        <img src="${item.image}" alt="${item.name}" onerror="this.style.display='none'; this.nextElementSibling.style.display='flex';">
                        <i class="fas fa-box fallback-icon" style="display: none;"></i>
                    </div>
                    <div class="cart-item-info">
                        <div class="cart-item-name">${item.name}</div>
                        <div class="cart-item-price">$${item.price.toLocaleString()}</div>
                        <div class="cart-item-controls">
                            <button class="quantity-btn" onclick="updateQuantity('${item.id}', -1)">-</button>
                            <span class="quantity-display">${item.quantity}</span>
                            <button class="quantity-btn" onclick="updateQuantity('${item.id}', 1)">+</button>
                            <button class="remove-item" onclick="removeFromCart('${item.id}')">
                                <i class="fas fa-trash"></i>
                            </button>
                        </div>
                    </div>
                </div>
            `;
        }
        cartItems.innerHTML = cartHTML;
        
        // Actualizar total
        cartTotal.textContent = `$${totalPrice.toLocaleString()}`;
    }
    
    console.log('UI actualizada correctamente');
    console.log('=== FIN ACTUALIZAR UI ===');
}

// Eventos del carrito
document.getElementById('cartIcon').addEventListener('click', () => {
    document.getElementById('cartSidebar').classList.add('active');
    document.getElementById('cartOverlay').classList.add('active');
});

document.getElementById('cartClose').addEventListener('click', () => {
    document.getElementById('cartSidebar').classList.remove('active');
    document.getElementById('cartOverlay').classList.remove('active');
});

document.getElementById('cartOverlay').addEventListener('click', () => {
    document.getElementById('cartSidebar').classList.remove('active');
    document.getElementById('cartOverlay').classList.remove('active');
});

document.getElementById('cartCheckout').addEventListener('click', () => {
    if (cart.length === 0) {
        showNotification('Tu carrito está vacío', 'error');
        return;
    }
    
    // Crear mensaje para WhatsApp con los productos del carrito
    let message = '¡Hola! Me gustaría comprar los siguientes productos:\n\n';
    
    cart.forEach(item => {
        message += `• ${item.name} (x${item.quantity}) - $${(item.price * item.quantity).toLocaleString()}\n`;
    });
    
    const total = cart.reduce((sum, item) => sum + (item.price * item.quantity), 0);
    message += `\n💰 *Total: $${total.toLocaleString()}*\n\n`;
    message += 'Por favor, confirma la disponibilidad y el método de entrega. ¡Gracias!';
    
    // Abrir WhatsApp
    const whatsappURL = `https://wa.me/573104119101?text=${encodeURIComponent(message)}`;
    window.open(whatsappURL, '_blank');
    
    // Limpiar carrito después de la compra
    cart = [];
    updateCartUI();
    
    // Cerrar carrito
    document.getElementById('cartSidebar').classList.remove('active');
    document.getElementById('cartOverlay').classList.remove('active');
    
    showNotification('¡Pedido enviado! Te redirigimos a WhatsApp.', 'success');
});

// Animación de aparición de elementos
const observerOptions = {
    threshold: 0.1,
    rootMargin: '0px 0px -50px 0px'
};

const observer = new IntersectionObserver((entries) => {
    entries.forEach(entry => {
        if (entry.isIntersecting) {
            entry.target.style.opacity = '1';
            entry.target.style.transform = 'translateY(0)';
        }
    });
}, observerOptions);

// Aplicar animación a elementos
document.addEventListener('DOMContentLoaded', () => {
    const animatedElements = document.querySelectorAll('.service-card, .portfolio-item, .stat-item, .skill-item, .product-card');
    
    animatedElements.forEach(el => {
        el.style.opacity = '0';
        el.style.transform = 'translateY(30px)';
        el.style.transition = 'opacity 0.6s ease, transform 0.6s ease';
        observer.observe(el);
    });
});

// Contador animado para estadísticas
function animateCounter(element, target, duration = 2000) {
    let start = 0;
    const increment = target / (duration / 16);
    
    const timer = setInterval(() => {
        start += increment;
        if (start >= target) {
            element.textContent = target + (element.textContent.includes('+') ? '+' : '');
            clearInterval(timer);
        } else {
            element.textContent = Math.floor(start) + (element.textContent.includes('+') ? '+' : '');
        }
    }, 16);
}

// Activar contadores cuando sean visibles
const statsObserver = new IntersectionObserver((entries) => {
    entries.forEach(entry => {
        if (entry.isIntersecting) {
            const statNumber = entry.target.querySelector('h3');
            const text = statNumber.textContent;
            const number = parseInt(text.replace(/\D/g, ''));
            
            if (text.includes('M')) {
                animateCounter(statNumber, number, 2000);
                statNumber.textContent = number + 'M';
            } else if (text.includes('+')) {
                animateCounter(statNumber, number, 2000);
                statNumber.textContent = number + '+';
            } else if (text.includes(',')) {
                animateCounter(statNumber, number, 2000);
                statNumber.textContent = number.toLocaleString();
            } else {
                animateCounter(statNumber, number, 2000);
            }
            
            statsObserver.unobserve(entry.target);
        }
    });
}, { threshold: 0.5 });

document.querySelectorAll('.stat-item').forEach(stat => {
    statsObserver.observe(stat);
});

// Formulario de contacto
const contactForm = document.querySelector('.contact-form');
if (contactForm) {
    contactForm.addEventListener('submit', (e) => {
        e.preventDefault();
        
        // Obtener datos del formulario
        const formData = new FormData(contactForm);
        const name = formData.get('name');
        const phone = formData.get('phone');
        const petName = formData.get('pet-name');
        const service = formData.get('service');
        const message = formData.get('message');
        
        // Validación básica
        if (!name || !phone || !petName || !service || !message) {
            showNotification('Por favor, completa todos los campos', 'error');
            return;
        }
        
        if (!isValidPhone(phone)) {
            showNotification('Por favor, ingresa un número de teléfono válido', 'error');
            return;
        }
        
        // Crear mensaje para WhatsApp
        const whatsappMessage = `¡Hola! Me gustaría agendar una cita para mi mascota:
        
👤 *Nombre:* ${name}
📱 *Teléfono:* ${phone}
🐕 *Mascota:* ${petName}
💼 *Servicio:* ${service}
📝 *Mensaje:* ${message}

¡Espero su respuesta!`;
        
        // Abrir WhatsApp
        const whatsappURL = `https://wa.me/573104119101?text=${encodeURIComponent(whatsappMessage)}`;
        window.open(whatsappURL, '_blank');
        
        // Mostrar notificación de éxito
        showNotification('¡Solicitud enviada! Te redirigimos a WhatsApp para confirmar tu cita.', 'success');
        contactForm.reset();
    });
}

// Validar teléfono
function isValidPhone(phone) {
    const phoneRegex = /^[0-9\s\-\+\(\)]{7,15}$/;
    return phoneRegex.test(phone);
}

// Mostrar notificaciones
function showNotification(message, type = 'info') {
    // Crear elemento de notificación
    const notification = document.createElement('div');
    notification.className = `notification ${type}`;
    notification.textContent = message;
    
    // Agregar al DOM
    document.body.appendChild(notification);
    
    // Animar entrada
    setTimeout(() => {
        notification.classList.add('show');
    }, 100);
    
    // Remover después de 4 segundos
    setTimeout(() => {
        notification.classList.remove('show');
        setTimeout(() => {
            if (document.body.contains(notification)) {
                document.body.removeChild(notification);
            }
        }, 300);
    }, 4000);
}

// Efecto parallax suave en el hero
window.addEventListener('scroll', () => {
    const scrolled = window.pageYOffset;
    const heroImage = document.querySelector('.hero-avatar');
    
    if (heroImage && scrolled < window.innerHeight) {
        heroImage.style.transform = `translateY(${scrolled * 0.3}px)`;
    }
});

// Efecto de escritura para el título
function typeWriter(element, text, speed = 100) {
    let i = 0;
    element.innerHTML = '';
    
    function type() {
        if (i < text.length) {
            element.innerHTML += text.charAt(i);
            i++;
            setTimeout(type, speed);
        }
    }
    
    type();
}

// Activar efecto de escritura cuando la página carga
window.addEventListener('load', () => {
    const heroTitle = document.querySelector('.hero-title');
    if (heroTitle) {
        const originalText = heroTitle.textContent;
        typeWriter(heroTitle, originalText, 80);
    }
});

// Lazy loading para imágenes
document.addEventListener('DOMContentLoaded', () => {
    const images = document.querySelectorAll('img[src]');
    
    const imageObserver = new IntersectionObserver((entries) => {
        entries.forEach(entry => {
            if (entry.isIntersecting) {
                const img = entry.target;
                img.style.opacity = '0';
                img.style.transition = 'opacity 0.3s ease';
                
                img.onload = () => {
                    img.style.opacity = '1';
                };
                
                imageObserver.unobserve(img);
            }
        });
    });
    
    images.forEach(img => imageObserver.observe(img));
});

// Efecto hover para las tarjetas de servicio y productos
document.querySelectorAll('.service-card, .product-card').forEach(card => {
    card.addEventListener('mouseenter', () => {
        card.style.transform = 'translateY(-10px) scale(1.02)';
    });
    
    card.addEventListener('mouseleave', () => {
        card.style.transform = 'translateY(0) scale(1)';
    });
});

// Cursor personalizado para elementos interactivos
document.addEventListener('DOMContentLoaded', () => {
    const interactiveElements = document.querySelectorAll('a, button, .service-card, .portfolio-item, .product-card');
    
    interactiveElements.forEach(element => {
        element.addEventListener('mouseenter', () => {
            document.body.style.cursor = 'pointer';
        });
        
        element.addEventListener('mouseleave', () => {
            document.body.style.cursor = 'default';
        });
    });
});

// Función para mostrar/ocultar elementos según el scroll
function handleScrollAnimations() {
    const elements = document.querySelectorAll('.fade-in');
    
    elements.forEach(element => {
        const elementTop = element.getBoundingClientRect().top;
        const elementVisible = 150;
        
        if (elementTop < window.innerHeight - elementVisible) {
            element.classList.add('active');
        }
    });
}

window.addEventListener('scroll', handleScrollAnimations);

// Inicializar tooltips para iconos de habilidades
document.querySelectorAll('.skill-item').forEach(skill => {
    skill.addEventListener('mouseenter', (e) => {
        const tooltip = document.createElement('div');
        tooltip.className = 'tooltip';
        tooltip.textContent = `Experto en ${e.target.querySelector('span').textContent}`;
        tooltip.style.cssText = `
            position: absolute;
            background: #2c3e50;
            color: white;
            padding: 0;
            border-radius: 5px;
            font-size: 0.8rem;
            z-index: 1000;
            pointer-events: none;
            transform: translateX(-50%);
            white-space: nowrap;
        `;
        
        document.body.appendChild(tooltip);
        
        const rect = e.target.getBoundingClientRect();
        tooltip.style.left = rect.left + rect.width / 2 + 'px';
        tooltip.style.top = rect.top - 40 + 'px';
    });
    
    skill.addEventListener('mouseleave', () => {
        const tooltip = document.querySelector('.tooltip');
        if (tooltip) {
            document.body.removeChild(tooltip);
        }
    });
});

// Animación CSS para fadeIn
const style = document.createElement('style');
style.textContent = `
    @keyframes fadeIn {
        from { opacity: 0; transform: translateY(20px); }
        to { opacity: 1; transform: translateY(0); }
    }
`;
document.head.appendChild(style);

// Inicializar carrito vacío al cargar la página
document.addEventListener('DOMContentLoaded', () => {
    updateCartUI();
});
    </script>
</body>
</html>
