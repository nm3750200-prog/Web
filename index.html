<?php
declare(strict_types=1);
require __DIR__ . '/includes.php';
$products = load_products();
$categories = categories();
$q = trim((string)($_GET['q'] ?? ''));
$cat = trim((string)($_GET['cat'] ?? ''));
$visible = array_values(array_filter($products, function($p) use ($q, $cat) {
    if (empty($p['active'])) return false;
    $matchesCat = $cat === '' || ($p['category'] ?? '') === $cat;
    $hay = mb_strtolower(($p['name'] ?? '') . ' ' . ($p['description'] ?? '') . ' ' . ($p['brand'] ?? ''), 'UTF-8');
    $matchesQ = $q === '' || mb_strpos($hay, mb_strtolower($q, 'UTF-8')) !== false;
    return $matchesCat && $matchesQ;
}));
function wa_link(string $message): string {
    return 'https://wa.me/' . WHATSAPP_NUMBER . '?text=' . rawurlencode($message);
}
$siteName = SITE_NAME;
?>
<!doctype html>
<html lang="es-AR">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title><?= h($siteName) ?> | Repuestos y autopartes en Argentina</title>
<meta name="description" content="Catálogo online multimarca de repuestos y autopartes. Consultá disponibilidad, compatibilidad, precio y envío a toda Argentina por WhatsApp.">
<meta name="robots" content="index,follow">
<link rel="canonical" href="<?= h(SITE_URL) ?>/">
<meta property="og:type" content="website">
<meta property="og:title" content="<?= h($siteName) ?> | Repuestos y autopartes">
<meta property="og:description" content="Encontrá repuestos para tu vehículo y consultá por WhatsApp. Envíos a toda Argentina.">
<link rel="stylesheet" href="assets/style.css">
<script defer src="assets/app.js"></script>
</head>
<body>
<header class="topbar">
  <a class="brand" href="index.php"><span class="brand-mark">RA</span><span><?= h($siteName) ?><small>REPUESTOS Y AUTOPARTES</small></span></a>
  <nav><a href="#categorias">Categorías</a><a href="#catalogo">Catálogo</a><a href="#como-comprar">Cómo comprar</a></nav>
  <a class="button button-small" href="<?= h(wa_link('Hola, quiero consultar por un repuesto.')) ?>" target="_blank" rel="noopener">WhatsApp</a>
</header>
<main>
<section class="hero">
  <div class="hero-copy">
    <span class="eyebrow">TIENDA ONLINE · ARGENTINA</span>
    <h1>Encontrá el repuesto que tu vehículo necesita.</h1>
    <p>Catálogo multimarca y atención personalizada. Consultanos por compatibilidad, disponibilidad, precio y envío.</p>
    <div class="hero-actions"><a class="button" href="#catalogo">Ver catálogo <span>→</span></a><a class="text-link" href="<?= h(wa_link('Hola, necesito ayuda para encontrar un repuesto.')) ?>" target="_blank" rel="noopener">Necesito asesoramiento</a></div>
    <div class="trust-row"><span>✓ Atención por WhatsApp</span><span>✓ Envíos a toda Argentina</span></div>
  </div>
  <div class="hero-art" aria-label="Ilustración de autopartes">
    <div class="orbit orbit-one"></div><div class="orbit orbit-two"></div>
    <div class="part-card part-main"><span class="part-symbol">⚙</span><b>REPUESTOS</b><small>Multimarca</small></div>
    <div class="part-card part-mini"><span>✦</span><b>Calidad</b><small>y asesoramiento</small></div>
    <div class="hero-tag">Tu próximo repuesto<br><strong>está más cerca.</strong></div>
  </div>
</section>
<section class="benefits">
  <div><span class="benefit-icon">⌕</span><b>Buscá tu repuesto</b><small>Por nombre, marca o categoría.</small></div>
  <div><span class="benefit-icon">◉</span><b>Confirmá compatibilidad</b><small>Te ayudamos a verificarlo.</small></div>
  <div><span class="benefit-icon">➜</span><b>Recibí en tu domicilio</b><small>Consultá envíos a toda Argentina.</small></div>
</section>
<section class="section" id="categorias">
  <div class="section-heading"><div><span class="eyebrow">EXPLORÁ</span><h2>Repuestos por categoría</h2></div><p>Elegí el rubro y encontrá lo que necesitás.</p></div>
  <div class="category-grid">
  <?php foreach ($categories as $i => $c): ?>
    <a class="category-card" href="index.php?cat=<?= rawurlencode($c) ?>#catalogo"><span class="category-number"><?= sprintf('%02d', $i+1) ?></span><span class="category-icon"><?= h(category_icon($i)) ?></span><b><?= h($c) ?></b><span class="category-arrow">↗</span></a>
  <?php endforeach; ?>
  </div>
</section>
<section class="section catalog-section" id="catalogo">
  <div class="section-heading"><div><span class="eyebrow">CATÁLOGO ONLINE</span><h2>Productos disponibles</h2></div><p>Los precios y la disponibilidad se confirman al consultar.</p></div>
  <form class="searchbar" method="get" action="index.php#catalogo">
    <input type="search" name="q" value="<?= h($q) ?>" placeholder="Buscar por repuesto, marca o descripción..." aria-label="Buscar productos">
    <select name="cat" aria-label="Filtrar por categoría"><option value="">Todas las categorías</option><?php foreach($categories as $c): ?><option value="<?= h($c) ?>" <?= $cat===$c?'selected':'' ?>><?= h($c) ?></option><?php endforeach; ?></select>
    <button class="button" type="submit">Buscar</button>
  </form>
  <?php if ($visible): ?>
  <div class="product-grid">
    <?php foreach($visible as $p): ?>
    <article class="product-card">
      <div class="product-image"><?php if (!empty($p['image'])): ?><img src="<?= h($p['image']) ?>" alt="<?= h($p['name']) ?>" loading="lazy"><?php else: ?><span>⚙</span><?php endif; ?><small><?= h($p['category'] ?? 'Repuesto') ?></small></div>
      <div class="product-info"><span class="product-brand"><?= h($p['brand'] ?? 'MULTIMARCA') ?></span><h3><?= h($p['name']) ?></h3><p><?= h($p['description'] ?? '') ?></p><a class="button button-outline" href="<?= h(wa_link('Hola, quiero consultar por: ' . ($p['name'] ?? 'un repuesto') . '. ¿Me confirmás precio, disponibilidad y compatibilidad?')) ?>" target="_blank" rel="noopener">Consultar por WhatsApp ↗</a></div>
    </article>
    <?php endforeach; ?>
  </div>
  <?php else: ?>
  <div class="empty-state"><span>⚙</span><h3><?= $q || $cat ? 'No encontramos productos con esa búsqueda' : 'Estamos preparando el catálogo' ?></h3><p><?= $q || $cat ? 'Probá con otro término o consultanos directamente.' : 'Estamos incorporando productos. Escribinos y te ayudamos a encontrar el repuesto que buscás.' ?></p><a class="button" href="<?= h(wa_link('Hola, estoy buscando un repuesto. ¿Me pueden ayudar?')) ?>" target="_blank" rel="noopener">Consultar por WhatsApp</a></div>
  <?php endif; ?>
  <?php if ($q || $cat): ?><p class="clear-filter"><a href="index.php#catalogo">Limpiar filtros</a></p><?php endif; ?>
</section>
<section class="how-section" id="como-comprar">
  <div class="how-copy"><span class="eyebrow">SIMPLE Y DIRECTO</span><h2>Comprar es fácil.</h2><p>Te atendemos personalmente para ayudarte a elegir el repuesto correcto.</p><a class="button" href="<?= h(wa_link('Hola, quiero realizar una consulta por un repuesto.')) ?>" target="_blank" rel="noopener">Empezar consulta ↗</a></div>
  <div class="steps">
    <div class="step"><span>01</span><div><b>Buscá el producto</b><p>Explorá el catálogo o contanos qué necesitás.</p></div></div>
    <div class="step"><span>02</span><div><b>Confirmamos los detalles</b><p>Verificamos compatibilidad, precio y disponibilidad.</p></div></div>
    <div class="step"><span>03</span><div><b>Coordinamos tu compra</b><p>Acordamos el medio de pago y el envío por WhatsApp.</p></div></div>
  </div>
</section>
<section class="warranty"><div><span class="eyebrow">COMPRA CON INFORMACIÓN CLARA</span><h2>Garantía según cada producto.</h2><p>La cobertura puede ser de 1 a 5 meses, según el producto y las condiciones acordadas antes de la compra. Consultá siempre el plazo y las condiciones aplicables a tu repuesto.</p></div><span class="warranty-mark">✓</span></section>
<section class="cta"><div><span class="eyebrow">¿NO ENCONTRÁS LO QUE BUSCÁS?</span><h2>Lo buscamos con vos.</h2><p>Mandanos los datos del vehículo o una foto del repuesto.</p></div><a class="button button-light" href="<?= h(wa_link('Hola, necesito ayuda para encontrar un repuesto. Mi vehículo es:')) ?>" target="_blank" rel="noopener">Hablar por WhatsApp ↗</a></section>
</main>
<footer><div class="footer-main"><a class="brand brand-footer" href="index.php"><span class="brand-mark">RA</span><span><?= h($siteName) ?><small>REPUESTOS Y AUTOPARTES</small></span></a><p>Atención online y envíos a toda Argentina.</p><a href="<?= h(wa_link('Hola, quisiera hacer una consulta.')) ?>" target="_blank" rel="noopener">Contactar por WhatsApp ↗</a></div><div class="footer-bottom"><span>© <?= date('Y') ?> <?= h($siteName) ?>. Todos los derechos reservados.</span><span>La disponibilidad, precio, compatibilidad, garantía y envío se confirman antes de comprar.</span><a href="privacidad.php">Privacidad</a></div></footer>
<a class="floating-wa" href="<?= h(wa_link('Hola, quiero consultar por un repuesto.')) ?>" target="_blank" rel="noopener" aria-label="Consultar por WhatsApp">☏</a>
</body></html>
