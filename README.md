# jsconst products = [
  {
    name: "Paneer Tikka",
    price: 120,
    image: "https://via.placeholder.com/200x150?text=Paneer+Tikka"
  },
  {
    name: "Masala Dosa",
    price: 90,
    image: "https://via.placeholder.com/200x150?text=Masala+Dosa"
  },
  {
    name: "Gulab Jamun",
    price: 60,
    image: "https://via.placeholder.com/200x150?text=Gulab+Jamun"
  }
];

const container = document.getElementById("product-list");

products.forEach(p => {
  const div = document.createElement("div");
  div.className = "product";
  div.innerHTML = `
    <img src="${p.image}" alt="${p.name}">
    <h3>${p.name}</h3>
    <p class="price">₹${p.price}</p>
  `;
  container.appendChild(div);
});
