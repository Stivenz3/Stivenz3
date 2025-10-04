import { motion } from "framer-motion";
import { SiHtml5, SiCss3, SiJavascript, SiReact, SiSpringboot, SiMysql, SiGit, SiGithub, SiPostgresql, SiMongodb, SiIntellijidea, SiVuedotjs, SiPython, SiFlask, SiGooglecloud, SiWindows, SiPostman, SiNodedotjs, SiExpress } from "react-icons/si";

export default function PortfolioCard() {
  const techs = [
    { icon: <SiHtml5 />, color: "text-orange-500" },
    { icon: <SiCss3 />, color: "text-blue-500" },
    { icon: <SiJavascript />, color: "text-yellow-400" },
    { icon: <SiReact />, color: "text-cyan-400" },
    { icon: <SiVuedotjs />, color: "text-green-400" },
    { icon: <SiSpringboot />, color: "text-green-500" },
    { icon: <SiNodedotjs />, color: "text-green-600" },
    { icon: <SiExpress />, color: "text-gray-200" },
    { icon: <SiPython />, color: "text-blue-400" },
    { icon: <SiFlask />, color: "text-gray-400" },
    { icon: <SiMysql />, color: "text-blue-600" },
    { icon: <SiPostgresql />, color: "text-sky-600" },
    { icon: <SiMongodb />, color: "text-green-500" },
    { icon: <SiGit />, color: "text-red-500" },
    { icon: <SiGithub />, color: "text-white" },
    { icon: <SiIntellijidea />, color: "text-purple-400" },
    { icon: <SiPostman />, color: "text-orange-400" },
    { icon: <SiGooglecloud />, color: "text-blue-400" },
    { icon: <SiWindows />, color: "text-sky-500" },
  ];

  return (
    <div className="min-h-screen flex flex-col items-center justify-center bg-gradient-to-br from-gray-900 via-gray-800 to-black text-white p-6">
      <motion.h1
        className="text-4xl md:text-6xl font-bold mb-4 text-center"
        initial={{ opacity: 0, y: -30 }}
        animate={{ opacity: 1, y: 0 }}
      >
        Stiven Zarza
      </motion.h1>
      <motion.p
        className="max-w-2xl text-center mb-10 text-gray-300"
        initial={{ opacity: 0 }}
        animate={{ opacity: 1 }}
        transition={{ delay: 0.3 }}
      >
        Estudiante de Ingeniería de Sistemas y Computación con pasión por la
        arquitectura de software y el desarrollo escalable.
      </motion.p>
      <motion.div
        className="grid grid-cols-4 sm:grid-cols-6 md:grid-cols-8 gap-6 text-4xl"
        initial="hidden"
        animate="show"
        variants={{
          show: {
            transition: { staggerChildren: 0.08 },
          },
        }}
      >
        {techs.map((t, i) => (
          <motion.div
            key={i}
            className={`${t.color} hover:scale-125 transition-transform`}
            whileHover={{ rotate: 10 }}
            variants={{ hidden: { opacity: 0 }, show: { opacity: 1 } }}
          >
            {t.icon}
          </motion.div>
        ))}
      </motion.div>

      <div className="mt-12 text-center text-gray-400">
        <p>📫 zarzalol@hotmail.com</p>
        <a
          href="https://stiven-zarza.vercel.app/"
          className="text-blue-400 hover:underline"
        >
          stiven-zarza.vercel.app
        </a>
      </div>
    </div>
  );
}

