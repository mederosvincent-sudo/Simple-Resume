# Simple-Resume

<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Simple Resumes</title>

<script src="https://www.paypal.com/sdk/js?client-id=YOUR_CLIENT_ID&currency=USD"></script>

<style>
body { margin:0; font-family:Arial; background:#0b0b0b; color:#fff; }
header { padding:20px 40px; background:#111; }
.hero { text-align:center; padding:100px 20px; }
.btn { background:white; color:black; padding:12px 25px; text-decoration:none; }
.section { padding:60px 20px; text-align:center; }
.pricing { display:flex; flex-wrap:wrap; justify-content:center; gap:20px; }
.card { background:#161616; padding:20px; width:260px; border-radius:10px; }
#paypal-button-container-basic,
#paypal-button-container-standard,
#paypal-button-container-full { margin-top:15px; }
</style>
</head>

<body>

<header>
  <h2>Simple Resumes</h2>
</header>

<section class="hero">
  <h1>Premium Resumes. Simple Pricing.</h1>
  <p>Professional resumes without the high cost.</p>
</section>

<section class="section">
  <h2>Services</h2>

  <div class="pricing">

    <div class="card">
      <h3>Basic Resume</h3>
      <p>$10.99</p>
      <div id="paypal-button-container-basic"></div>
    </div>

    <div class="card">
      <h3>Resume + Cover Letter</h3>
      <p>$19.99</p>
      <div id="paypal-button-container-standard"></div>
    </div>

    <div class="card">
      <h3>Full Package</h3>
      <p>$29.99</p>
      <div id="paypal-button-container-full"></div>
    </div>

  </div>
</section>

<section class="section">
  <h2>Before & After</h2>
  <p>We turn messy resumes into clean, professional ones that get interviews.</p>
</section>

<section class="section">
  <h2>Contact</h2>
  <p>Email: simpleresumes@email.com</p>
</section>

<script>
paypal.Buttons({
  createOrder: function(data, actions) {
    return actions.order.create({
      purchase_units: [{ amount: { value: '10.99' } }]
    });
  }
}).render('#paypal-button-container-basic');

paypal.Buttons({
  createOrder: function(data, actions) {
    return actions.order.create({
      purchase_units: [{ amount: { value: '19.99' } }]
    });
  }
}).render('#paypal-button-container-standard');

paypal.Buttons({
  createOrder: function(data, actions) {
    return actions.order.create({
      purchase_units: [{ amount: { value: '29.99' } }]
    });
  }
}).render('#paypal-button-container-full');
</script>

</body>
</html>
