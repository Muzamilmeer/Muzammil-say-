<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Bandipora Fish Valley</title>
</head>
<body style="font-family: sans-serif; text-align: center; background-color: #e0f7fa; padding: 20px;">

  <h1>🐟 Bandipora Fish Valley 🐟</h1>
  <h3>Fresh Trout | Fingerlings | Rainbow Trout</h3>

  <!-- Fish Cards -->
  <div>
    <h2>Available Fishes</h2>
    <button onclick="buyNow('Rainbow Trout')">Buy Rainbow Trout</button><br><br>
    <button onclick="buyNow('Fingerlings')">Buy Fingerlings</button><br><br>
    <button onclick="buyNow('Live Trout')">Buy Live Trout</button>
  </div>

  <hr style="margin: 40px 0;">

  <!-- Inquiry Form -->
  <div>
    <h2>Inquiry Form</h2>
    <form onsubmit="sendWhatsApp(event)">
      <input type="text" id="name" placeholder="Your Name" required style="padding: 10px; width: 90%;"><br><br>
      <input type="tel" id="phone" placeholder="Phone Number" required style="padding: 10px; width: 90%;"><br><br>
      <input type="text" id="quantity" placeholder="Quantity / Fish Type" required style="padding: 10px; width: 90%;"><br><br>
      <textarea id="message" placeholder="Additional Message..." style="padding: 10px; width: 90%; height: 100px;"></textarea><br><br>
      <button type="submit" style="padding: 10px 20px;">Send Inquiry</button>
    </form>
  </div>

  <script>
    // WhatsApp Buy Now button
    function buyNow(fishName) {
      const msg = `🐟 *Buy Now - Bandipora Fish Valley* 🐟\n\n🛒 Fish: ${fishName}\n📦 Please provide quantity & address.`;
      const url = `https://wa.me/919149915607?text=${encodeURIComponent(msg)}`;
      location.href = url; // ✅ Works inside Kodular WebView
    }

    // WhatsApp Inquiry Form
    function sendWhatsApp(event) {
      event.preventDefault();
      const name = document.getElementById('name').value;
      const phone = document.getElementById('phone').value;
      const quantity = document.getElementById('quantity').value;
      const message = document.getElementById('message').value;

      const fullMsg = `🐟 *Fish Inquiry - Bandipora Fish Valley* 🐟\n\n👤 Name: ${name}\n📞 Phone: ${phone}\n📦 Order: ${quantity}\n📝 Message: ${message}`;
      const url = `https://wa.me/919149915607?text=${encodeURIComponent(fullMsg)}`;
      location.href = url; // ✅ Opens WhatsApp properly
    }
  </script>
</body>
</html>
