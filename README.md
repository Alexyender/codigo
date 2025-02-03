# codigo
san valentin
import { useState } from "react";
import { motion } from "framer-motion";
import { Button } from "@/components/ui/button";

export default function LoveApp() {
  const [showMessage, setShowMessage] = useState(false);

  return (
    <div className="flex flex-col items-center justify-center min-h-screen bg-pink-200 p-6">
      <motion.h1 
        className="text-4xl font-bold text-red-600 mb-4"
        initial={{ scale: 0 }}
        animate={{ scale: 1 }}
        transition={{ duration: 0.5 }}
      >
        ¡Feliz San Valentín! 💖
      </motion.h1>
      <motion.p 
        className="text-lg text-gray-700 mb-6"
        initial={{ opacity: 0 }}
        animate={{ opacity: 1 }}
        transition={{ duration: 1 }}
      >
        Este mensaje es para alguien especial. 💕
      </motion.p>
      <Button
        className="bg-red-500 hover:bg-red-600 text-white px-4 py-2 rounded-lg"
        onClick={() => setShowMessage(true)}
      >
        Haz clic para ver tu sorpresa 🎁
      </Button>
      {showMessage && (
        <motion.div 
          className="mt-6 p-4 bg-white shadow-md rounded-lg text-center"
          initial={{ scale: 0 }}
          animate={{ scale: 1 }}
          transition={{ duration: 0.4 }}
        >
          <p className="text-lg text-gray-700">Te quiero muchísimo! 💘</p>
        </motion.div>
      )}
    </div>
  );
}
