import React from "react"; import { motion } from "framer-motion"; import { Phone, CheckCircle2 } from "lucide-react";

// ✅ Landing de una sola página para JH Transporte // Colores corporativos: naranja (#FF6600), negro, blanco // Incluye secciones: Hero, Servicios, Flota (placeholder para fotos), Clientes, Nosotros, PyMEs, Contacto

const features = [ { title: "Transporte refrigerado", desc: "Camiones con equipos de frío, manteniendo la cadena de frío garantizada (-20°C a +6°C).", }, { title: "Cobertura nacional", desc: "Rutas en todo el país con seguimiento satelital.", }, { title: "Seguridad", desc: "Protocolos de higiene, estiba segura y choferes profesionales.", }, { title: "Puntualidad", desc: "Cumplimiento de horarios y entregas confiables.", }, ];

const gallery = [ "/images/camion1.jpg", "/images/camion2.jpg", "/images/camion3.jpg", ];

export default function JHTransporteLanding() { const whatsapp = "https://wa.me/5493510000000?text=Hola%20JH%20Transporte,%20quisiera%20pedir%20un%20presupuesto";

return ( <div className="font-sans bg-white text-gray-900"> {/* Hero */} <section className="bg-black text-white min-h-screen flex flex-col justify-center items-center text-center p-6"> <motion.img src="/images/logo.png" alt="JH Transporte" className="w-40 mb-6" initial={{ opacity: 0, y: -30 }} animate={{ opacity: 1, y: 0 }} transition={{ duration: 1 }} /> <h1 className="text-4xl md:text-6xl font-bold text-[#FF6600]"> Transporte refrigerado de confianza </h1> <p className="mt-4 text-lg max-w-xl"> Soluciones logísticas seguras y puntuales en toda Argentina. </p> <a
href={whatsapp}
target="_blank"
className="mt-6 inline-flex items-center gap-2 bg-[#FF6600] text-white px-6 py-3 rounded-2xl shadow-lg hover:bg-orange-600 transition"
> <Phone /> Contactar por WhatsApp </a> </section>

{/* Servicios */}
  <section className="py-20 px-6 bg-gray-50">
    <h2 className="text-3xl font-bold text-center mb-12 text-[#FF6600]">
      Nuestros Servicios
    </h2>
    <div className="grid md:grid-cols-2 lg:grid-cols-4 gap-8 max-w-6xl mx-auto">
      {features.map((f, i) => (
        <motion.div
          key={i}
          className="bg-white rounded-2xl p-6 shadow-md border border-gray-200"
          initial={{ opacity: 0, y: 20 }}
          whileInView={{ opacity: 1, y: 0 }}
          transition={{ duration: 0.5, delay: i * 0.2 }}
        >
          <CheckCircle2 className="text-[#FF6600] mb-4" size={32} />
          <h3 className="font-bold text-xl mb-2">{f.title}</h3>
          <p className="text-gray-600">{f.desc}</p>
        </motion.div>
      ))}
    </div>
  </section>

  {/* Galería de fotos */}
  <section className="py-20 px-6">
    <h2 className="text-3xl font-bold text-center mb-12 text-[#FF6600]">
      Nuestra Flota
    </h2>
    <div className="grid md:grid-cols-3 gap-6 max-w-6xl mx-auto">
      {gallery.map((src, i) => (
        <motion.img
          key={i}
          src={src}
          alt={`Camión ${i + 1}`}
          className="rounded-2xl shadow-md border border-gray-200 object-cover w-full h-64"
          initial={{ opacity: 0 }}
          whileInView={{ opacity: 1 }}
          transition={{ duration: 0.6, delay: i * 0.2 }}
        />
      ))}
    </div>
  </section>

  {/* Clientes */}
  <section className="py-20 px-6 bg-gray-50">
    <h2 className="text-3xl font-bold text-center mb-12 text-[#FF6600]">
      Clientes que confían en nosotros
    </h2>
    <p className="text-center max-w-2xl mx-auto text-gray-700">
      Trabajamos con empresas líderes en la industria alimenticia y de logística, como <strong>Biomac</strong>.
    </p>
  </section>

  {/* Nosotros */}
  <section className="py-20 px-6">
    <h2 className="text-3xl font-bold text-center mb-12 text-[#FF6600]">
      Sobre nosotros
    </h2>
    <div className="max-w-4xl mx-auto text-center text-gray-700">
      <p>
        En <strong>JH Transporte</strong> somos una empresa familiar dedicada al transporte de carga refrigerada en toda Argentina. Nuestro compromiso es brindar un servicio confiable, seguro y puntual, cuidando la calidad de cada entrega.
      </p>
    </div>
  </section>

  {/* PyMEs */}
  <section className="py-20 px-6 bg-[#FF6600] text-white text-center">
    <h2 className="text-3xl font-bold mb-6">Apoyamos a las empresas que están creciendo</h2>
    <p className="max-w-3xl mx-auto mb-6">
      Sabemos lo que significa empezar. Si tu empresa es nueva o está en expansión, comunicate con nosotros:
      podemos armarte una propuesta especial para que tengas un transporte confiable desde el día uno.
    </p>
    <a
      href={whatsapp}
      target="_blank"
      className="inline-flex items-center gap-2 bg-white text-[#FF6600] px-6 py-3 rounded-2xl shadow-lg hover:bg-gray-100 transition"
    >
      <Phone /> Quiero mi propuesta especial
    </a>
  </section>

  {/* Contacto */}
  <section className="py-20 px-6 bg-black text-white text-center">
    <h2 className="text-3xl font-bold mb-6 text-[#FF6600]">Contacto</h2>
    <p className="mb-6">Escribinos para solicitar un presupuesto o hacer tu consulta.</p>
    <a
      href={whatsapp}
      target="_blank"
      className="inline-flex items-center gap-2 bg-[#FF6600] text-white px-6 py-3 rounded-2xl shadow-lg hover:bg-orange-600 transition"
    >
      <Phone /> Contactar por WhatsApp
    </a>
  </section>
</div>

); }

