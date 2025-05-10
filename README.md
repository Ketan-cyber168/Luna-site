#luna–site
import { Card, CardContent } from "@/components/ui/card";
import { Button } from "@/components/ui/button";
import { motion } from "framer-motion";

export default function LunaProductPage() {
  return (
    <div className="min-h-screen bg-black text-white p-6 font-sans">
      <header className="text-center mb-10">
        <h1 className="text-4xl md:text-6xl font-bold tracking-wide">Luna</h1>
        <p className="text-lg text-gray-400 mt-2">Premium Clothing for the Bold</p>
      </header>

      <section className="grid md:grid-cols-3 gap-8 max-w-6xl mx-auto">
        {[1, 2, 3].map((item) => (
          <motion.div
            key={item}
            whileHover={{ scale: 1.05, rotate: 1 }}
            className="transition-transform"
          >
            <Card className="bg-zinc-900 rounded-2xl overflow-hidden shadow-lg">
              <img
                src={`https://via.placeholder.com/400x500?text=Product+${item}`}
                alt={`Luna Product ${item}`}
                className="w-full h-80 object-cover"
              />
              <CardContent className="p-4">
                <h2 className="text-xl font-semibold mb-2">Luna Tee {item}</h2>
                <p className="text-gray-400 mb-4">Soft cotton, sleek fit, premium design.</p>
                <Button className="w-full bg-white text-black font-semibold hover:bg-gray-200">
                  Shop Now
                </Button>
              </CardContent>
            </Card>
          </motion.div>
        ))}
      </section>

      <footer className="text-center text-gray-500 mt-16 text-sm">
        &copy; {new Date().getFullYear()} Luna. All rights reserved.
      </footer>
    </div>
  );
}
