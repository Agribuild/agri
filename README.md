import React from "react";
import { Button } from "@/components/ui/button";
import { Card, CardContent } from "@/components/ui/card";

export default function HomePage() {
  return (
    <main className="flex flex-col items-center justify-center p-6 space-y-12">
      {/* Hero Section */}
      <section className="w-full bg-green-800 text-white p-14 rounded-2xl shadow-xl text-center">
        <h1 className="text-5xl font-extrabold mb-4">Agribuild Pros</h1>
        <p className="text-xl mb-6">Greenhouse Construction & Irrigation Systems Built for Growth</p>
        <div className="space-x-4">
          <Button className="bg-white text-green-800 font-bold">Get a Free Quote</Button>
          <Button variant="outline" className="text-white border-white">View Our Work</Button>
        </div>
      </section>

      {/* About Us Preview */}
      <section className="max-w-3xl text-center">
        <h2 className="text-3xl font-semibold mb-2">Who We Are</h2>
        <p className="text-gray-700 mb-4">
          Agribuild Pros specializes in designing and building state-of-the-art greenhouses and precision irrigation
          systems. Our mission is to empower growers with sustainable and efficient infrastructure that fuels their success.
        </p>
        <Button variant="outline">More About Us</Button>
      </section>

      {/* Services Overview */}
      <section className="w-full max-w-6xl">
        <h2 className="text-2xl font-semibold mb-6 text-center">Our Services</h2>
        <div className="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-4 gap-6">
          {[
            { title: "Greenhouse Design", desc: "Custom-built greenhouses tailored to your crops and climate." },
            { title: "Irrigation Installation", desc: "Drip and overhead systems designed for efficiency and yield." },
            { title: "Agricultural Structures", desc: "From seedling shelters to grow tunnels and more." },
            { title: "Maintenance & Repairs", desc: "Reliable servicing to keep your systems running smoothly." }
          ].map((service, index) => (
            <Card key={index} className="rounded-2xl shadow-md">
              <CardContent className="p-6">
                <h3 className="text-lg font-semibold mb-2">{service.title}</h3>
                <p className="text-sm text-gray-600">{service.desc}</p>
              </CardContent>
            </Card>
          ))}
        </div>
      </section>

      {/* Featured Projects */}
      <section className="w-full max-w-4xl text-center">
        <h2 className="text-2xl font-semibold mb-4">Recent Projects</h2>
        <p className="text-gray-600 mb-6">Take a look at some of our recent builds and installations.</p>
        <div className="grid grid-cols-1 md:grid-cols-2 gap-4">
          <div className="bg-gray-200 rounded-xl h-48 flex items-center justify-center">Greenhouse – Berry Farm</div>
          <div className="bg-gray-200 rounded-xl h-48 flex items-center justify-center">Irrigation – Vegetable Grower</div>
        </div>
      </section>

      {/* Why Choose Us */}
      <section className="max-w-3xl text-center">
        <h2 className="text-2xl font-semibold mb-4">Why Choose Agribuild Pros</h2>
        <ul className="text-gray-700 space-y-2">
          <li>✔️ Proven industry expertise</li>
          <li>✔️ Customized, scalable solutions</li>
          <li>✔️ Commitment to sustainability</li>
          <li>✔️ Exceptional customer service</li>
        </ul>
      </section>

      {/* Call to Action */}
      <section className="bg-green-100 rounded-2xl p-8 text-center max-w-3xl">
        <h3 className="text-xl font-bold mb-4">Let’s grow your operation together.</h3>
        <Button className="bg-green-800 text-white">Request a Free Consultation</Button>
      </section>

      {/* Footer */}
      <footer className="text-center text-sm text-gray-500 mt-12">
        &copy; {new Date().getFullYear()} Agribuild Pros. All rights reserved.
      </footer>
    </main>
  );
}
