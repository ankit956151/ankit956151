import React, { useState, useEffect } from 'react';
import { 
  Github, 
  Linkedin, 
  Twitter, 
  Mail, 
  MapPin, 
  Code, 
  Database, 
  Layout, 
  Terminal, 
  Coffee, 
  ExternalLink,
  Server,
  Cpu,
  Globe
} from 'lucide-react';

const Portfolio = () => {
  const [activeSection, setActiveSection] = useState('home');

  // Smooth scroll handler
  const scrollToSection = (id) => {
    const element = document.getElementById(id);
    if (element) {
      element.scrollIntoView({ behavior: 'smooth' });
      setActiveSection(id);
    }
  };

  return (
    <div className="min-h-screen bg-[#0d1117] text-[#c9d1d9] font-sans selection:bg-[#1f6feb] selection:text-white">
      {/* Navigation */}
      <nav className="sticky top-0 z-50 bg-[#161b22]/90 backdrop-blur-md border-b border-[#30363d]">
        <div className="max-w-6xl mx-auto px-4 h-16 flex items-center justify-between">
          <div className="flex items-center gap-2 font-bold text-xl text-[#58a6ff]">
            <Terminal size={24} />
            <span>Ankit<span className="text-[#c9d1d9]">Pandey</span></span>
          </div>
          <div className="hidden md:flex gap-6 text-sm font-semibold">
            {['About', 'Tech Stack', 'Projects', 'Stats', 'Contact'].map((item) => (
              <button
                key={item}
                onClick={() => scrollToSection(item.toLowerCase().replace(' ', '-'))}
                className="hover:text-[#58a6ff] transition-colors"
              >
                {item}
              </button>
            ))}
          </div>
        </div>
      </nav>

      <main className="max-w-6xl mx-auto px-4 py-10 space-y-24">
        
        {/* Header / Hero Section */}
        <header id="about" className="flex flex-col items-center text-center space-y-6 animate-fade-in">
          <div className="relative group">
            <div className="absolute -inset-1 bg-gradient-to-r from-[#58a6ff] to-purple-600 rounded-full blur opacity-25 group-hover:opacity-75 transition duration-1000 group-hover:duration-200"></div>
            <img 
              src="https://avatars.githubusercontent.com/u/ankit956151?v=4" 
              alt="Ankit Pandey" 
              className="relative w-32 h-32 rounded-full border-4 border-[#30363d] shadow-xl"
              onError={(e) => e.target.src = "https://ui-avatars.com/api/?name=Ankit+Pandey&background=0D1117&color=58a6ff"}
            />
            <div className="absolute bottom-0 right-0 bg-[#238636] w-6 h-6 rounded-full border-4 border-[#0d1117]" title="Available for hire"></div>
          </div>

          <div className="space-y-4">
            <h1 className="text-4xl md:text-5xl font-extrabold tracking-tight">
              Hi, I'm Ankit Pandey <img src="https://raw.githubusercontent.com/MartinHeinz/MartinHeinz/master/wave.gif" width="30" height="30" alt="wave" className="inline-block mb-2" />
            </h1>
            
            <div className="h-12 flex items-center justify-center">
              <img 
                src="https://readme-typing-svg.herokuapp.com/?lines=PHP+Developer+from+Mumbai;HTML5+%7C+CSS3+%7C+JavaScript+%7C+jQuery;Bootstrap+%7C+PHP+%7C+MySQL+%7C+XAMPP;Building+Dynamic+Web+Applications&font=Roboto&size=22&duration=3500&pause=1000&center=true&width=650&height=50&color=58a6ff" 
                alt="Typing SVG" 
                className="max-w-full"
              />
            </div>

            {/* Social Badges */}
            <div className="flex flex-wrap justify-center gap-3 pt-4">
              <a href="https://github.com/ankit956151" target="_blank" rel="noreferrer" className="transition-transform hover:scale-105">
                <img src="https://img.shields.io/github/followers/ankit956151?label=Follow&style=for-the-badge&logo=github&color=238636&labelColor=161b22" alt="GitHub followers" />
              </a>
              <a href="https://www.linkedin.com/in/ankit-pandey-1b0ba1215/" target="_blank" rel="noreferrer" className="transition-transform hover:scale-105">
                <img src="https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white&labelColor=161b22" alt="LinkedIn" />
              </a>
              <a href="https://x.com/Sit124A" target="_blank" rel="noreferrer" className="transition-transform hover:scale-105">
                <img src="https://img.shields.io/badge/Twitter-Follow-1DA1F2?style=for-the-badge&logo=twitter&logoColor=white&labelColor=161b22" alt="Twitter" />
              </a>
              <img src="https://komarev.com/ghpvc/?username=ankit956151&label=Profile%20views&color=0e75b6&style=for-the-badge" alt="Profile views" className="hidden sm:inline-block" />
            </div>
          </div>
        </header>

        {/* About & Code Snippet Grid */}
        <section className="grid grid-cols-1 lg:grid-cols-2 gap-10 items-start">
          <div className="space-y-6">
            <h2 className="text-2xl font-bold flex items-center gap-2 text-[#c9d1d9] border-b border-[#30363d] pb-2">
               About Me
            </h2>
            <div className="flex flex-col md:flex-row gap-6 items-center md:items-start text-[#8b949e] leading-relaxed">
              <div className="flex-1 space-y-4">
                <p>
                  I'm a passionate <strong className="text-[#58a6ff]">PHP Developer</strong> from <strong className="text-[#c9d1d9]">Mumbai, Maharashtra</strong>, focused on creating dynamic web applications with clean, responsive design.
                </p>
                <ul className="space-y-2 list-disc list-inside marker:text-[#58a6ff]">
                  <li>🌍 Based in <span className="text-[#c9d1d9]">Nalasopara East, Mumbai</span></li>
                  <li>🔭 Working on <span className="text-[#c9d1d9]">Shopping Sites & Forum Systems</span></li>
                  <li>🌱 Learning <span className="text-[#c9d1d9]">Advanced PHP & Optimization</span></li>
                  <li>⚡ Fun fact: I love building UI designs!</li>
                </ul>
              </div>
              <img 
                src="https://cdn.dribbble.com/users/1162077/screenshots/3848914/programmer.gif" 
                alt="Coding GIF" 
                className="w-48 rounded-lg shadow-lg border border-[#30363d]"
              />
            </div>
          </div>

          {/* PHP Class Code Block */}
          <div className="relative group">
            <div className="absolute -inset-0.5 bg-gradient-to-r from-[#58a6ff] to-[#bc8cff] rounded-lg blur opacity-30 group-hover:opacity-50 transition duration-200"></div>
            <div className="relative rounded-lg bg-[#0d1117] border border-[#30363d] overflow-hidden">
              <div className="flex items-center gap-2 px-4 py-2 bg-[#161b22] border-b border-[#30363d]">
                <div className="w-3 h-3 rounded-full bg-[#ff5f56]"></div>
                <div className="w-3 h-3 rounded-full bg-[#ffbd2e]"></div>
                <div className="w-3 h-3 rounded-full bg-[#27c93f]"></div>
                <span className="ml-2 text-xs text-[#8b949e] font-mono">Profile.php</span>
              </div>
              <div className="p-4 overflow-x-auto">
                <pre className="font-mono text-sm leading-relaxed">
                  <span className="text-[#ff7b72]">&lt;?php</span>
                  <br/>
                  <span className="text-[#ff7b72]">class</span> <span className="text-[#d2a8ff]">AnkitPandey</span> {'{'}
                  <br/>
                  {'    '}<span className="text-[#ff7b72]">public</span> <span className="text-[#79c0ff]">$name</span> = <span className="text-[#a5d6ff]">"Ankit Pandey"</span>;
                  <br/>
                  {'    '}<span className="text-[#ff7b72]">public</span> <span className="text-[#79c0ff]">$role</span> = <span className="text-[#a5d6ff]">"PHP Developer"</span>;
                  <br/>
                  {'    '}<span className="text-[#ff7b72]">public</span> <span className="text-[#79c0ff]">$stack</span> = [
                  <br/>
                  {'        '}<span className="text-[#a5d6ff]">"PHP"</span>, <span className="text-[#a5d6ff]">"MySQL"</span>, <span className="text-[#a5d6ff]">"JavaScript"</span>
                  <br/>
                  {'    '}];
                  <br/>
                  {'    '}<span className="text-[#ff7b72]">public</span> <span className="text-[#ff7b72]">function</span> <span className="text-[#d2a8ff]">dailyRoutine</span>() {'{'}
                  <br/>
                  {'        '}<span className="text-[#ff7b72]">return</span> [
                  <br/>
                  {'            '}<span className="text-[#a5d6ff]">"☕ Coffee"</span>,
                  <br/>
                  {'            '}<span className="text-[#a5d6ff]">"💻 Code"</span>,
                  <br/>
                  {'            '}<span className="text-[#a5d6ff]">"🔄 Repeat"</span>
                  <br/>
                  {'        '}];
                  <br/>
                  {'    '}{'}'}
                  <br/>
                  {'}'}
                  <br/>
                  <span className="text-[#ff7b72]">?&gt;</span>
                </pre>
              </div>
            </div>
          </div>
        </section>

        {/* Tech Stack */}
        <section id="tech-stack" className="space-y-8">
          <div className="text-center space-y-2">
            <h2 className="text-3xl font-bold">Tech Stack & Tools</h2>
            <div className="h-1 w-20 bg-[#58a6ff] mx-auto rounded-full"></div>
          </div>

          <div className="bg-[#161b22] border border-[#30363d] rounded-xl p-6 shadow-sm">
            <div className="flex flex-col items-center gap-6">
              <h3 className="text-[#8b949e] font-semibold uppercase tracking-wider text-sm">Core Technologies</h3>
              <div className="flex flex-wrap justify-center gap-4">
                <img src="https://skillicons.dev/icons?i=html,css,js,jquery,bootstrap,php,mysql&theme=dark" alt="Tech Stack Icons" className="hover:scale-105 transition-transform duration-300" />
              </div>
              
              <div className="w-full h-px bg-[#30363d]"></div>
              
              <h3 className="text-[#8b949e] font-semibold uppercase tracking-wider text-sm">Environment</h3>
              <div className="flex gap-4">
                 <img src="https://img.shields.io/badge/XAMPP-FB7A24?style=for-the-badge&logo=xampp&logoColor=white" alt="XAMPP" />
                 <img src="https://img.shields.io/badge/Apache-D22128?style=for-the-badge&logo=apache&logoColor=white" alt="Apache" />
              </div>
            </div>
          </div>
        </section>

        {/* Featured Projects */}
        <section id="projects" className="space-y-8">
          <div className="flex items-center gap-3 mb-6">
            <h2 className="text-3xl font-bold">Featured Projects</h2>
            <span className="px-3 py-1 text-xs font-semibold text-[#58a6ff] border border-[#58a6ff] rounded-full bg-[#58a6ff]/10">Public Repos</span>
          </div>

          <div className="grid grid-cols-1 md:grid-cols-2 gap-6">
            {/* Project 1: Shopping Site */}
            <div className="bg-[#161b22] border border-[#30363d] rounded-xl overflow-hidden hover:border-[#58a6ff] transition-colors group flex flex-col">
              <div className="p-6 flex-1 space-y-4">
                <div className="flex justify-between items-start">
                  <div>
                     <h3 className="text-xl font-bold flex items-center gap-2">
                       <Layout size={20} className="text-[#58a6ff]" /> Shopping Site
                     </h3>
                     <p className="text-[#8b949e] text-sm mt-1">E-commerce Platform</p>
                  </div>
                  <a href="https://github.com/ankit956151/Shopping_site" className="text-[#8b949e] hover:text-[#58a6ff]">
                    <ExternalLink size={20} />
                  </a>
                </div>
                
                {/* JS Code Snippet Decor */}
                <div className="bg-[#0d1117] rounded-lg p-3 border border-[#30363d] font-mono text-xs">
                  <div className="text-[#79c0ff]">const project = {'{'}</div>
                  <div className="pl-4 text-[#c9d1d9]">type: <span className="text-[#a5d6ff]">'E-commerce'</span>,</div>
                  <div className="pl-4 text-[#c9d1d9]">features: [<span className="text-[#a5d6ff]">'Cart'</span>, <span className="text-[#a5d6ff]">'Checkout'</span>]</div>
                  <div className="text-[#79c0ff]">{'}'};</div>
                </div>

                <div className="flex flex-wrap gap-2 pt-2">
                   {['JavaScript', 'jQuery', 'Bootstrap', 'HTML5'].map(tag => (
                     <span key={tag} className="px-2 py-1 bg-[#30363d]/50 text-[#8b949e] text-xs rounded-md">{tag}</span>
                   ))}
                </div>
              </div>
            </div>

            {/* Project 2: Forum System */}
            <div className="bg-[#161b22] border border-[#30363d] rounded-xl overflow-hidden hover:border-[#58a6ff] transition-colors group flex flex-col">
              <div className="p-6 flex-1 space-y-4">
                <div className="flex justify-between items-start">
                  <div>
                     <h3 className="text-xl font-bold flex items-center gap-2">
                       <Globe size={20} className="text-[#58a6ff]" /> Forum System
                     </h3>
                     <p className="text-[#8b949e] text-sm mt-1">Community Discussion Platform</p>
                  </div>
                  <a href="https://github.com/ankit956151/forum" className="text-[#8b949e] hover:text-[#58a6ff]">
                    <ExternalLink size={20} />
                  </a>
                </div>

                {/* PHP Code Snippet Decor */}
                <div className="bg-[#0d1117] rounded-lg p-3 border border-[#30363d] font-mono text-xs">
                  <div className="text-[#79c0ff]">$features = [</div>
                  <div className="pl-4 text-[#a5d6ff]">'User Auth'</div>
                  <div className="pl-4 text-[#a5d6ff]">'Post Replies'</div>
                  <div className="pl-4 text-[#a5d6ff]">'Topic Categorization'</div>
                  <div className="text-[#79c0ff]">];</div>
                </div>

                <div className="flex flex-wrap gap-2 pt-2">
                   {['PHP', 'MySQL', 'Bootstrap', 'Auth'].map(tag => (
                     <span key={tag} className="px-2 py-1 bg-[#30363d]/50 text-[#8b949e] text-xs rounded-md">{tag}</span>
                   ))}
                </div>
              </div>
            </div>
            
            {/* Small Projects Row */}
            <div className="md:col-span-2 grid grid-cols-1 md:grid-cols-2 gap-6">
              <div className="bg-[#161b22] border border-[#30363d] p-5 rounded-lg flex items-start gap-4 hover:bg-[#1c2128] transition-colors">
                <Database className="text-[#58a6ff] shrink-0 mt-1" />
                <div>
                  <h4 className="font-bold text-[#c9d1d9] mb-1">CRUD Operations System</h4>
                  <p className="text-sm text-[#8b949e] mb-2">Complete Create, Read, Update, Delete functionality with secure queries.</p>
                  <a href="https://github.com/ankit956151/crud-using-php" className="text-xs text-[#58a6ff] hover:underline">View Repository →</a>
                </div>
              </div>

              <div className="bg-[#161b22] border border-[#30363d] p-5 rounded-lg flex items-start gap-4 hover:bg-[#1c2128] transition-colors">
                <Layout className="text-[#58a6ff] shrink-0 mt-1" />
                <div>
                  <h4 className="font-bold text-[#c9d1d9] mb-1">Grocery Store UI</h4>
                  <p className="text-sm text-[#8b949e] mb-2">Clean, modern responsive interfaces for grocery stores.</p>
                  <a href="https://github.com/ankit956151/grocery-store-ui" className="text-xs text-[#58a6ff] hover:underline">View Repository →</a>
                </div>
              </div>
            </div>
          </div>
        </section>

        {/* GitHub Stats */}
        <section id="stats" className="space-y-6 text-center">
          <h2 className="text-3xl font-bold flex items-center justify-center gap-3">
             <Server size={28} /> GitHub Analytics
          </h2>
          
          <div className="flex flex-col md:flex-row justify-center items-center gap-4">
             <img className="h-44 w-full md:w-auto object-contain" src="https://github-readme-stats.vercel.app/api?username=ankit956151&show_icons=true&theme=tokyonight&include_all_commits=true&count_private=true" alt="GitHub Stats" />
             <img className="h-44 w-full md:w-auto object-contain" src="https://github-readme-stats.vercel.app/api/top-langs/?username=ankit956151&layout=compact&langs_count=6&theme=tokyonight" alt="Top Langs" />
          </div>
          
          <div className="flex justify-center w-full overflow-hidden">
            <img src="https://streak-stats.demolab.com/?user=ankit956151&theme=tokyonight" alt="Streak Stats" className="max-w-full" />
          </div>

          <div className="pt-4">
             <img src="https://github-readme-activity-graph.vercel.app/graph?username=ankit956151&theme=tokyo-night" alt="Activity Graph" className="w-full rounded-lg" />
          </div>
        </section>

        {/* Development Philosophy (Visual Diagram) */}
        <section className="bg-[#161b22] border border-[#30363d] rounded-2xl p-8">
            <h2 className="text-2xl font-bold mb-8 text-center">Development Workflow</h2>
            
            {/* Custom Diagram using CSS Grid/Flex instead of Mermaid */}
            <div className="flex flex-wrap justify-center gap-4 mb-8">
              {['Plan & Design', 'Create UI', 'Build Backend', 'Database', 'Test & Debug', 'Deploy'].map((step, index) => (
                <div key={step} className="flex items-center">
                  <div className="bg-[#0d1117] border border-[#58a6ff] px-4 py-3 rounded-lg text-sm font-semibold text-[#58a6ff] shadow-[0_0_10px_rgba(88,166,255,0.2)]">
                    {step}
                  </div>
                  {index !== 5 && (
                    <div className="w-8 h-0.5 bg-[#30363d] mx-1 hidden sm:block"></div>
                  )}
                  {index !== 5 && (
                     <div className="sm:hidden block mx-auto text-[#30363d] px-2">↓</div>
                  )}
                </div>
              ))}
            </div>

            <div className="grid md:grid-cols-3 gap-6 text-sm text-[#8b949e]">
              <div className="p-4 bg-[#0d1117] rounded-lg border border-[#30363d]">
                <strong className="text-[#c9d1d9] block mb-1">🎨 UI-First Approach</strong>
                Design clean, responsive interfaces before coding logic.
              </div>
              <div className="p-4 bg-[#0d1117] rounded-lg border border-[#30363d]">
                <strong className="text-[#c9d1d9] block mb-1">🔧 CRUD Mastery</strong>
                Focus on solid database operations and security.
              </div>
              <div className="p-4 bg-[#0d1117] rounded-lg border border-[#30363d]">
                <strong className="text-[#c9d1d9] block mb-1">🔒 Clean Code</strong>
                Maintainable, well-structured PHP architectures.
              </div>
            </div>
        </section>

        {/* Footer / Contact */}
        <footer id="contact" className="text-center space-y-8 pb-10">
          <div className="bg-gradient-to-b from-[#161b22] to-[#0d1117] border border-[#30363d] rounded-2xl p-8 max-w-2xl mx-auto">
             <h2 className="text-3xl font-bold mb-2">Let's Connect</h2>
             <p className="text-[#8b949e] mb-6">Open to collaboration on E-commerce & Community Platforms</p>
             
             <div className="flex flex-wrap justify-center gap-4 mb-6">
                <a href="mailto:ankit.pandey01409@gmail.com" className="flex items-center gap-2 bg-[#d14836] text-white px-5 py-2 rounded-md hover:opacity-90 transition-opacity">
                  <Mail size={18} /> Email
                </a>
                <a href="https://www.linkedin.com/in/ankit-pandey-1b0ba1215/" className="flex items-center gap-2 bg-[#0077b5] text-white px-5 py-2 rounded-md hover:opacity-90 transition-opacity">
                  <Linkedin size={18} /> LinkedIn
                </a>
                <a href="https://github.com/ankit956151" className="flex items-center gap-2 bg-[#24292e] text-white px-5 py-2 rounded-md hover:opacity-90 transition-opacity">
                  <Github size={18} /> GitHub
                </a>
             </div>

             <div className="flex items-center justify-center gap-2 text-[#8b949e] text-sm">
               <MapPin size={16} /> Mumbai, Maharashtra, India
             </div>
          </div>

          <div className="space-y-4">
            <div className="font-mono text-xs text-[#8b949e] bg-[#161b22] inline-block px-4 py-2 rounded-lg border border-[#30363d]">
               <span className="text-[#ff7b72]">echo</span> <span className="text-[#a5d6ff]">"Thanks for visiting my profile!"</span>;
            </div>
            
            {/* Snake Animation fallback handling - pointing to a generic raw generated file logic or local placeholder if raw fails */}
            <div className="flex justify-center grayscale opacity-60 hover:grayscale-0 hover:opacity-100 transition-all duration-500">
               <img src="https://raw.githubusercontent.com/ankit956151/ankit956151/output/github-contribution-grid-snake.svg" alt="Snake Animation" onError={(e) => e.target.style.display = 'none'} />
            </div>

            <p className="text-xs text-[#8b949e]">
              &copy; {new Date().getFullYear()} Ankit Pandey. Built with React & Tailwind.
            </p>
          </div>
        </footer>

      </main>
    </div>
  );
};

export default Portfolio;
