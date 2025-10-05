import { BrowserRouter as Router, Routes, Route } from "react-router-dom";
import Navbar from "./components/Navbar";
import Footer from "./components/Footer";
import Home from "./pages/Home";
import About from "./pages/About";
import Programs from "./pages/Programs";
import Mentorship from "./pages/Mentorship";
import Blog from "./pages/Blog";
import Gallery from "./pages/Gallery";
import Contact from "./pages/Contact";

function App() {
  return (
    <Router>
      <div className="flex flex-col min-h-screen bg-gray-50">
        <Navbar />
        <main className="flex-grow">
          <Routes>
            <Route path="/" element={<Home />} />
            <Route path="/about" element={<About />} />
            <Route path="/programs" element={<Programs />} />
            <Route path="/mentorship" element={<Mentorship />} />
            <Route path="/blog" element={<Blog />} />
            <Route path="/gallery" element={<Gallery />} />
            <Route path="/contact" element={<Contact />} />
          </Routes>
        </main>
        <Footer />
      </div>
    </Router>
  );
}

export default App;
import { Link } from "react-router-dom";

const Navbar = () => (
  <nav className="bg-blue-900 text-white shadow-md">
    <div className="max-w-7xl mx-auto px-4 py-4 flex justify-between items-center">
      <h1 className="text-xl font-bold">Inua Nurse Footprint (INF)</h1>
      <div className="space-x-4">
        <Link to="/" className="hover:text-blue-300">Home</Link>
        <Link to="/about" className="hover:text-blue-300">About</Link>
        <Link to="/programs" className="hover:text-blue-300">Programs</Link>
        <Link to="/mentorship" className="hover:text-blue-300">Mentorship</Link>
        <Link to="/blog" className="hover:text-blue-300">Blog</Link>
        <Link to="/gallery" className="hover:text-blue-300">Gallery</Link>
        <Link to="/contact" className="hover:text-blue-300">Contact</Link>
      </div>
    </div>
  </nav>
);

export default Navbar;
const Footer = () => (
  <footer className="bg-blue-950 text-gray-200 py-8">
    <div className="max-w-7xl mx-auto text-center space-y-2">
      <p>&copy; {new Date().getFullYear()} Inua Nurse Footprint (INF)</p>
      <p>#TheNextGenerationOfNurses | #UpliftTheNurseToUpliftTheCommunity</p>
      <a href="mailto:inf.go.ke@gmail.com" className="hover:text-blue-300">inf.go.ke@gmail.com</a>
    </div>
  </footer>
);

export default Footer;
const Home = () => (
  <div className="text-center py-20 bg-gradient-to-b from-blue-800 to-blue-500 text-white">
    <h2 className="text-4xl font-bold mb-4">Welcome to Inua Nurse Footprint (INF)</h2>
    <p className="max-w-3xl mx-auto text-lg">
      Empowering and uplifting the next generation of nurses through mentorship, training,
      innovation, and collaboration. Together, we can leave no nurse behind.
    </p>
    <img src="/images/hero-nurse.jpg" alt="Nurse Team" className="mx-auto mt-10 rounded-2xl shadow-lg w-3/4" />
  </div>
);

export default Home;
import { useState } from "react";

const Blog = () => {
  const [posts] = useState([
    {
      id: 1,
      title: "INF Mentorship Program Launches Nationwide",
      date: "Sept 30, 2025",
      summary: "INF officially rolled out its mentorship and clinical skill-building program across nursing schools.",
      image: "/images/blog1.jpg",
    },
    {
      id: 2,
      title: "World Patient Safety Day – INF at USIU",
      date: "Sept 17, 2025",
      summary: "Students trained on safe newborn and child care practices in collaboration with MOH and WHO.",
      image: "/images/blog2.jpg",
    },
  ]);

  return (
    <div className="max-w-6xl mx-auto px-4 py-16">
      <h2 className="text-3xl font-bold text-blue-900 mb-8 text-center">INF Blog & News</h2>
      <div className="grid md:grid-cols-2 gap-8">
        {posts.map((post) => (
          <div key={post.id} className="bg-white shadow-md rounded-xl overflow-hidden hover:shadow-xl transition">
            <img src={post.image} alt={post.title} className="w-full h-56 object-cover" />
            <div className="p-6">
              <h3 className="text-xl font-semibold text-blue-900">{post.title}</h3>
              <p className="text-gray-500 text-sm mb-2">{post.date}</p>
              <p className="text-gray-700">{post.summary}</p>
              <button className="mt-4 text-blue-700 font-medium hover:underline">Read More</button>
            </div>
          </div>
        ))}
      </div>
    </div>
  );
};

export default Blog;
const Gallery = () => {
  const images = [
    "/images/gallery1.jpg",
    "/images/gallery2.jpg",
    "/images/gallery3.jpg",
    "/images/gallery4.jpg",
  ];

  return (
    <div className="max-w-6xl mx-auto px-4 py-16">
      <h2 className="text-3xl font-bold text-blue-900 mb-8 text-center">INF Gallery</h2>
      <div className="grid grid-cols-2 md:grid-cols-3 gap-4">
        {images.map((img, index) => (
          <img
            key={index}
            src={img}
            alt={`INF event ${index + 1}`}
            className="rounded-xl shadow-md hover:scale-105 transition-transform duration-300"
          />
        ))}
      </div>
    </div>
  );
};

export default Gallery;
const About = () => (
  <div className="max-w-6xl mx-auto px-4 py-16">
    <h2 className="text-3xl font-bold text-blue-900 mb-6 text-center">About Inua Nurse Footprint (INF)</h2>
    <p className="text-gray-700 text-lg mb-6">
      Inua Nurse Footprint (INF) is a student-led nursing organisation uniting nursing students across Kenya and Africa. We inspire, mentor, and equip the next generation of nurses for excellence in service and leadership.
    </p>
    <ul className="list-disc list-inside text-gray-700 mb-6">
      <li><strong>Mission:</strong> Empower nursing students through mentorship, training, and collaborative opportunities.</li>
      <li><strong>Vision:</strong> A united, empowered nursing community driving sustainable healthcare impact across Africa.</li>
      <li><strong>Slogans:</strong> #TheNextGenerationOfNurses | #UpliftTheNurseToUpliftTheCommunity | #LeaveNoNurseBehind</li>
    </ul>
    <img src="/images/about_team.jpg" alt="INF Team" className="rounded-2xl shadow-md w-full" />
  </div>
);

export default About;
const Programs = () => {
  const programs = [
    {
      title: "Clinical Mentorship",
      description: "Connecting students with experienced nurses for hands-on mentorship and professional growth.",
      image: "/images/program_mentorship.jpg",
    },
    {
      title: "Community Outreach",
      description: "Medical camps, health education, and awareness programs in underserved communities.",
      image: "/images/program_outreach.jpg",
    },
    {
      title: "Emergency & First Aid Training",
      description: "Practical workshops on life-saving skills, neonatal care, and emergency preparedness.",
      image: "/images/program_training.jpg",
    },
  ];

  return (
    <div className="max-w-6xl mx-auto px-4 py-16">
      <h2 className="text-3xl font-bold text-blue-900 mb-10 text-center">INF Programs</h2>
      <div className="grid md:grid-cols-3 gap-8">
        {programs.map((p, i) => (
          <div key={i} className="bg-white rounded-2xl shadow-md overflow-hidden hover:shadow-lg transition">
            <img src={p.image} alt={p.title} className="w-full h-56 object-cover" />
            <div className="p-6">
              <h3 className="text-xl font-semibold text-blue-900">{p.title}</h3>
              <p className="text-gray-700 mt-2">{p.description}</p>
            </div>
          </div>
        ))}
      </div>
    </div>
  );
};

export default Programs;
const Mentorship = () => {
  const mentors = [
    { name: "Charles Mutsotso", year: "4th Year", phone: "798750811", email: "Itscharly97@gmail.com" },
    { name: "Jane Wanjiku", year: "3rd Year", phone: "0712345678", email: "jwanjiku@gmail.com" },
  ];

  return (
    <div className="max-w-6xl mx-auto px-4 py-16">
      <h2 className="text-3xl font-bold text-blue-900 mb-10 text-center">Mentorship Program</h2>
      <p className="text-gray-700 text-lg mb-8 text-center">
        INF connects experienced nursing students and professionals with junior students for guidance, clinical skill development, and career advice.
      </p>
      <div className="grid md:grid-cols-2 gap-8">
        {mentors.map((m, i) => (
          <div key={i} className="bg-white rounded-2xl shadow-md p-6 hover:shadow-lg transition">
            <h3 className="text-xl font-semibold text-blue-900">{m.name}</h3>
            <p className="text-gray-700">Year: {m.year}</p>
            <p className="text-gray-700">Phone: {m.phone}</p>
            <p className="text-gray-700">Email: {m.email}</p>
          </div>
        ))}
      </div>
      <div className="mt-10 text-center">
        <img src="/images/mentorship.jpg" alt="Mentorship" className="rounded-2xl shadow-md mx-auto w-3/4" />
      </div>
    </div>
  );
};

export default Mentorship;
const Contact = () => (
  <div className="max-w-3xl mx-auto px-4 py-16">
    <h2 className="text-3xl font-bold text-blue-900 mb-6 text-center">Contact INF</h2>
    <p className="text-gray-700 text-center mb-6">
      For partnership inquiries, mentorship applications, or general information, reach out to INF.
    </p>
    <form className="bg-white p-8 rounded-2xl shadow-md space-y-4">
      <input type="text" placeholder="Full Name" className="w-full border px-4 py-2 rounded-md" />
      <input type="email" placeholder="Email Address" className="w-full border px-4 py-2 rounded-md" />
      <textarea placeholder="Message" rows="5" className="w-full border px-4 py-2 rounded-md"></textarea>
      <button type="submit" className="w-full bg-blue-900 text-white py-2 rounded-md hover:bg-blue-700 transition">
        Send Message
      </button>
    </form>
    <div className="mt-8 text-center text-gray-700">
      <p>Email: <a href="mailto:inf.go.ke@gmail.com" className="text-blue-900 underline">inf.go.ke@gmail.com</a></p>
      <p>Phone: +254 112569560</p>
    </div>
  </div>
);

export default Contact;
