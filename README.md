import { Shield, Terminal, Lock } from 'lucide-react';
import TypeWriter from './TypeWriter';

const HeroSection = () => {
  const typewriterTexts = [
    'Cybersecurity Enthusiast',
    'Penetration Tester in Training',
    'Network Security Learner',
    'Always curious, always hacking!',
  ];

  return (
    <section className="relative min-h-screen flex items-center justify-center px-6 py-20">
      <div className="relative z-10 text-center max-w-4xl mx-auto">
        {/* Terminal-style header */}
        <div className="terminal-window p-6 mb-8 inline-block">
          <div className="flex items-center gap-2 mb-4 pb-3 border-b border-primary/20">
            <div className="w-3 h-3 rounded-full bg-red-500" />
            <div className="w-3 h-3 rounded-full bg-yellow-500" />
            <div className="w-3 h-3 rounded-full bg-green-500" />
            <span className="ml-4 text-muted-foreground font-mono text-sm">
              ~/jeffrey-shalom
            </span>
          </div>
          <code className="text-primary font-mono text-sm">
            <span className="text-secondary">$</span> whoami
          </code>
        </div>

        {/* Name */}
        <h1 className="text-5xl md:text-7xl font-bold mb-4 tracking-tight">
          <span className="gradient-text">Jeffrey Shalom</span>
        </h1>

        {/* Animated subtitle */}
        <div className="text-xl md:text-2xl font-mono h-12 mb-8">
          <TypeWriter texts={typewriterTexts} />
        </div>

        {/* Location badge */}
        <div className="flex items-center justify-center gap-2 mb-8">
          <span className="cyber-badge px-4 py-2 rounded-full font-mono text-sm flex items-center gap-2">
            <Shield className="w-4 h-4" />
            India 🇮🇳
          </span>
        </div>

        {/* Status cards */}
        <div className="flex flex-wrap justify-center gap-4 mb-10">
          <div className="cyber-badge-green px-4 py-2 rounded-lg font-mono text-sm flex items-center gap-2">
            <Terminal className="w-4 h-4" />
            Learning: Network Security & Ethical Hacking
          </div>
          <div className="cyber-badge-purple px-4 py-2 rounded-lg font-mono text-sm flex items-center gap-2">
            <Lock className="w-4 h-4" />
            Open for Collaborations
          </div>
        </div>

        {/* CTA */}
        <a
          href="mailto:jeffshalom06@gmail.com"
          className="inline-flex items-center gap-2 px-8 py-4 bg-primary text-primary-foreground font-semibold rounded-lg box-glow hover:scale-105 transition-transform duration-300"
        >
          <Terminal className="w-5 h-5" />
          Let's Connect
        </a>
      </div>
    </section>
  );
};

export default HeroSection;
