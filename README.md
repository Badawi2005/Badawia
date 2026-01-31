import { Card, CardContent } from "@/components/ui/card";
import { Button } from "@/components/ui/button";
import { motion } from "framer-motion";
import {
  ShoppingCart,
  Phone,
  MessageCircle,
  ShieldCheck,
  Truck,
  Egg,
} from "lucide-react";

const WA_NUMBER = "6282132698172";

export default function BadawiFarmWebsite() {
  return (
    <div className="min-h-screen bg-gradient-to-b from-[#0f172a] to-[#020617] text-white">

      {/* FLOATING WHATSAPP (DESKTOP ONLY) */}
      <a
        href={`https://wa.me/${WA_NUMBER}?text=Halo%20Badawi%20Farm,%20saya%20ingin%20order%20telur`}
        target="_blank"
        rel="noopener noreferrer"
        className="hidden md:flex fixed bottom-6 right-6 z-50 items-center gap-2 bg-green-500 hover:bg-green-600 px-5 py-3 rounded-full shadow-2xl transition"
      >
        <MessageCircle /> WhatsApp
      </a>

      {/* HERO */}
      <section className="container mx-auto px-4 md:px-6 py-20 md:py-24 text-center">
        <motion.h1
          initial={{ opacity: 0, y: 24 }}
          animate={{ opacity: 1, y: 0 }}
          transition={{ duration: 0.8 }}
          className="text-4xl md:text-6xl font-bold tracking-wide"
        >
          BADAWI FARM
        </motion.h1>
        <p className="mt-6 text-lg text-slate-300 max-w-2xl mx-auto">
          Supplier Telur Ayam Berkualitas • Grosir & Eceran
        </p>
        <div className="mt-8 md:mt-10 flex flex-col sm:flex-row justify-center gap-4">
          <Button
            className="rounded-2xl px-8 py-6"
            onClick={() =>
              window.open(`https://wa.me/${WA_NUMBER}`, "_blank")
            }
          >
            <ShoppingCart className="mr-2" /> Pesan Sekarang
          </Button>
          <Button
            variant="outline"
            className="rounded-2xl px-8 py-6"
            onClick={() =>
              window.open(
                `https://wa.me/${WA_NUMBER}?text=Halo%20Badawi%20Farm,%20saya%20ingin%20bertanya`,
                "_blank"
              )
            }
          >
            <Phone className="mr-2" /> Hubungi Kami
          </Button>
        </div>
      </section>

      {/* KEUNGGULAN */}
      <section className="container mx-auto px-4 md:px-6 py-16 md:py-20">
        <h2 className="text-3xl font-semibold text-center mb-12">
          Kenapa Pilih Badawi Farm?
        </h2>
        <div className="grid md:grid-cols-3 gap-8">
          {[{ icon: Egg, title: "Telur Segar", desc: "Langsung dari peternakan" }, { icon: ShieldCheck, title: "Kualitas Terjaga", desc: "Sortir & standar kebersihan" }, { icon: Truck, title: "Pengiriman Cepat", desc: "Siap kirim area sekitar" }].map((item, i) => (
            <Card key={i} className="bg-white/5 border-white/10 rounded-2xl hover:scale-[1.02] transition">
              <CardContent className="p-8 text-center">
                <item.icon className="mx-auto mb-4 text-amber-400" size={36} />
                <h3 className="text-xl font-semibold mb-2">{item.title}</h3>
                <p className="text-slate-300 text-sm">{item.desc}</p>
              </CardContent>
            </Card>
          ))}
        </div>
      </section>

      {/* HARGA */}
      <section className="container mx-auto px-4 md:px-6 py-16 md:py-20">
        <h2 className="text-3xl font-semibold text-center mb-12">Harga Telur</h2>
        <div className="grid md:grid-cols-3 gap-8">
          {[{ title: "Eceran", price: "Tanya Admin WhatsApp" }, { title: "Grosir", price: "Tanya Admin WhatsApp" }, { title: "Grosir Besar", price: "Tanya Admin WhatsApp" }].map((item, i) => (
            <Card key={i} className="bg-white/5 border-white/10 rounded-2xl hover:scale-[1.02] transition">
              <CardContent className="p-8 text-center">
                <h3 className="text-xl font-semibold mb-4">{item.title}</h3>
                <p className="text-2xl font-bold text-amber-400">{item.price}</p>
                <Button
                  className="mt-6 rounded-xl"
                  onClick={() => window.open(`https://wa.me/${WA_NUMBER}`, "_blank")}
                >
                  Order via WhatsApp
                </Button>
              </CardContent>
            </Card>
          ))}
        </div>
        <p className="text-center text-sm text-slate-400 mt-6">
          *Harga dapat berubah mengikuti pasar
        </p>
      </section>

      {/* PEMBAYARAN */}
      <section className="container mx-auto px-4 md:px-6 py-16 md:py-20">
        <h2 className="text-3xl font-semibold text-center mb-12">Metode Pembayaran</h2>
        <div className="grid md:grid-cols-3 gap-8">
          {[{ title: "Transfer Bank", desc: "BCA • BRI • Mandiri • BNI" }, { title: "E-Wallet", desc: "ShopeePay • DANA" }, { title: "Crypto", desc: "USDT • BTC • ETH" }].map((item, i) => (
            <Card key={i} className="bg-white/5 border-white/10 rounded-2xl">
              <CardContent className="p-8 text-center">
                <h3 className="text-xl font-semibold mb-3">{item.title}</h3>
                <p className="text-slate-300 text-sm">{item.desc}</p>
                <p className="mt-2 text-slate-400 text-sm">Detail via WhatsApp</p>
              </CardContent>
            </Card>
          ))}
        </div>
        <div className="text-center mt-10">
          <Button
            className="rounded-xl"
            onClick={() =>
              window.open(
                `https://wa.me/${WA_NUMBER}?text=Halo%20Badawi%20Farm,%20saya%20ingin%20konfirmasi%20pembayaran`,
                "_blank"
              )
            }
          >
            Konfirmasi Pembayaran
          </Button>
        </div>
      </section>

      {/* FOOTER */}
      <footer className="container mx-auto px-4 md:px-6 py-16 text-center text-slate-400">
        <p className="text-lg font-semibold text-white">BADAWI FARM</p>
        <p className="mt-2">Peternakan & Supplier Telur Ayam</p>
        <p className="mt-4 text-sm">© {new Date().getFullYear()} Badawi Farm</p>
      </footer>
    {/* STICKY CTA MOBILE */}
      <div className="fixed bottom-0 left-0 right-0 z-50 md:hidden bg-[#020617]/90 backdrop-blur border-t border-white/10 px-4 py-3">
        <Button
          className="w-full rounded-xl py-6 text-base"
          onClick={() => window.open(`https://wa.me/${WA_NUMBER}`, "_blank")}
        >
          <ShoppingCart className="mr-2" /> Order via WhatsApp
        </Button>
      </div>
    </div>
  );
}
