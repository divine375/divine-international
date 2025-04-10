import { Card, CardContent } from "@/components/ui/card";
import { Button } from "@/components/ui/button";
import { Input } from "@/components/ui/input";
import { Textarea } from "@/components/ui/textarea";
import { Mail, Phone, Globe, MessageSquare, Star, MapPin } from "lucide-react";
import { Helmet } from "react-helmet";

export default function DivineInternational() {
  return (
    <div className="p-6 space-y-12">
      <Helmet>
        <title>Divine International – Exporting Quality Worldwide</title>
        <meta
          name="description"
          content="Divine International exports quality food, fruits, leather goods, and bathroom accessories worldwide. Trusted by global clients."
        />
        <meta
          name="keywords"
          content="divine international, import export, food export, leather products, bathroom accessories export, fruits exporter"
        />
        <meta name="author" content="Divine International" />
        <meta property="og:title" content="Divine International – Exporting Quality Worldwide" />
        <meta
          property="og:description"
          content="Food, Fruits, Leather & Bathroom Accessories Exporter from India."
        />
        <meta property="og:image" content="https://divine-international.vercel.app/images/logo.png" />
        <meta property="og:url" content="https://divine-international.vercel.app" />
        <meta name="twitter:card" content="summary_large_image" />
        <meta name="robots" content="index, follow" />
      </Helmet>

      {/* Hero Section */}
      <section className="text-center py-12 bg-gradient-to-r from-green-100 to-blue-100 rounded-2xl shadow-md">
        <img
          src="/images/logo.png"
          alt="Divine International Logo"
          className="mx-auto mb-4 w-24 h-24"
        />
        <h1 className="text-4xl font-bold mb-2">Divine International</h1>
        <p className="text-lg text-gray-700 max-w-2xl mx-auto">
          YOUR TRUSTED EXPORT PARTNER – Food, Fruits, Bathroom Accessories, and Leather Goods
        </p>
      </section>

      {/* Products Section */}
      <section>
        <h2 className="text-2xl font-semibold mb-6">Our Products</h2>
        <div className="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-6">
          {[...
            { name: "Fresh Fruits", price: "$20 / box", image: "/images/fruits.jpg" },
            { name: "Basmati Rice", price: "$30 / 5kg", image: "/images/rice.jpg" },
            { name: "Luxury Faucets", price: "$45 / piece", image: "/images/faucet.jpg" },
            { name: "Leather Wallet", price: "$25 / piece", image: "/images/wallet.jpg" },
            { name: "Mango Pulp", price: "$15 / can", image: "/images/mango.jpg" },
            { name: "Shower Heads", price: "$35 / piece", image: "/images/shower.jpg" },
            { name: "Leather Belts", price: "$20 / piece", image: "/images/belt.jpg" },
            { name: "Spices Pack", price: "$10 / pouch", image: "/images/spices.jpg" },
          ].map((product) => (
            <Card key={product.name} className="rounded-2xl shadow">
              <img src={product.image} alt={product.name} className="rounded-t-2xl w-full h-40 object-cover" />
              <CardContent className="p-4">
                <h3 className="text-xl font-semibold">{product.name}</h3>
                <p className="text-green-700 font-medium">{product.price}</p>
              </CardContent>
            </Card>
          ))}
        </div>
      </section>

      {/* Why Choose Us */}
      <section className="bg-blue-50 p-6 rounded-2xl shadow-md">
        <h2 className="text-2xl font-semibold mb-4">Why Choose Divine International?</h2>
        <ul className="list-disc pl-6 text-gray-700 space-y-2">
          <li>High-quality products with international standards</li>
          <li>Fast and reliable global shipping</li>
          <li>Transparent pricing with no hidden fees</li>
          <li>Customer satisfaction is our top priority</li>
        </ul>
      </section>

      {/* Testimonials Section */}
      <section className="bg-white p-6 rounded-2xl shadow-md">
        <h2 className="text-2xl font-semibold mb-4">What Our Clients Say</h2>
        <div className="grid md:grid-cols-2 gap-6">
          {[...
            { name: "John Smith", feedback: "High quality and timely delivery! Very professional team." },
            { name: "Aarav Patel", feedback: "Excellent customer service and great packaging. Highly recommended." },
          ].map((review) => (
            <Card key={review.name} className="rounded-2xl shadow">
              <CardContent className="p-4">
                <div className="flex gap-2 items-center mb-2 text-yellow-500">
                  {[...Array(5)].map((_, i) => (
                    <Star key={i} className="w-4 h-4 fill-yellow-500" />
                  ))}
                </div>
                <p className="text-gray-700 italic">"{review.feedback}"</p>
                <p className="text-sm font-semibold mt-2 text-gray-900">– {review.name}</p>
              </CardContent>
            </Card>
          ))}
        </div>
      </section>

      {/* Google Map Section */}
      <section className="bg-gray-50 p-6 rounded-2xl shadow-md">
        <h2 className="text-2xl font-semibold mb-4 flex items-center gap-2"><MapPin className="w-5 h-5" /> Our Location</h2>
        <iframe
          src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d241317.11609802198!2d72.74110184291165!3d19.08219783984226!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x3be7b63c4b6a159f%3A0xcef54f4f47b51b69!2sMumbai%2C%20Maharashtra!5e0!3m2!1sen!2sin!4v1681135149873!5m2!1sen!2sin"
          width="100%"
          height="300"
          style={{ border: 0 }}
          allowFullScreen=""
          loading="lazy"
          referrerPolicy="no-referrer-when-downgrade"
          className="rounded-xl"
        ></iframe>
      </section>

      {/* Contact Section */}
      <section className="bg-gray-100 p-6 rounded-2xl shadow-md">
        <h2 className="text-2xl font-semibold mb-4">Contact Us</h2>
        <div className="grid md:grid-cols-2 gap-6">
          <form className="space-y-4">
            <Input placeholder="Your Name" />
            <Input placeholder="Your Email" type="email" />
            <Textarea placeholder="Your Message" />
            <Button className="w-full">Send Message</Button>
          </form>
          <div className="space-y-4 text-gray-700">
            <p className="flex items-center gap-2"><Phone className="w-5 h-5" /> +91-9876543210</p>
            <p className="flex items-center gap-2"><Mail className="w-5 h-5" /> contact@divineinternational.com</p>
            <p className="flex items-center gap-2"><Globe className="w-5 h-5" /> Location: Mumbai, India</p>
            <a
              href="https://wa.me/919876543210"
              target="_blank"
              rel="noopener noreferrer"
              className="inline-flex items-center gap-2 text-green-700 font-semibold hover:underline"
            >
              <MessageSquare className="w-5 h-5" /> Chat on WhatsApp
            </a>
          </div>
        </div>
      </section>

      {/* Footer */}
      <footer className="text-center text-gray-500 text-sm pt-6 border-t">
        © 2025 Divine International. All rights reserved.
      </footer>
    </div>
  );
}
