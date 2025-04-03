import Link from "next/link"
import {
  ArrowRight,
  Award,
  BarChart,
  CheckCircle,
  FileText,
  Globe,
  Layers,
  Lightbulb,
  Rocket,
  Star,
  Target,
  Zap,
} from "lucide-react"

import { Button } from "@/components/ui/button"
import { Badge } from "@/components/ui/badge"

export default function Home() {
  return (
    <div className="flex min-h-screen flex-col bg-white">
      {/* Header avec navigation */}
      <header className="sticky top-0 z-50 w-full border-b bg-white/95 backdrop-blur supports-[backdrop-filter]:bg-white/60">
        <div className="container flex h-16 items-center justify-between">
          <div className="flex items-center gap-2">
            <FileText className="h-6 w-6 text-primary" />
            <span className="font-bold text-xl">CV Analyzer Pro</span>
          </div>
          <nav className="hidden md:flex items-center gap-8">
            <Link href="#features" className="text-sm font-medium text-gray-600 hover:text-primary transition-colors">
              Fonctionnalités
            </Link>
            <Link
              href="#testimonials"
              className="text-sm font-medium text-gray-600 hover:text-primary transition-colors"
            >
              Témoignages
            </Link>
            <Link href="#pricing" className="text-sm font-medium text-gray-600 hover:text-primary transition-colors">
              Tarifs
            </Link>
            <Link href="#faq" className="text-sm font-medium text-gray-600 hover:text-primary transition-colors">
              FAQ
            </Link>
          </nav>
          <div className="flex items-center gap-4">
            <Link
              href="/login"
              className="text-sm font-medium text-gray-600 hover:text-primary transition-colors hidden md:inline-flex"
            >
              Se connecter
            </Link>
            <Link href="/register">
              <Button className="rounded-full shadow-md hover:shadow-lg transition-all">Commencer gratuitement</Button>
            </Link>
          </div>
        </div>
      </header>

      <main className="flex-1">
        {/* Hero Section */}
        <section className="relative overflow-hidden bg-gradient-to-b from-white to-gray-50 py-20 md:py-32">
          <div className="absolute inset-0 bg-grid-gray-100/50 bg-[size:24px_24px] opacity-25"></div>
          <div className="container relative">
            <div className="mx-auto max-w-4xl text-center">
              <Badge className="mb-4 rounded-full px-4 py-1.5 text-sm font-medium">Propulsé par l'IA • Nouveau</Badge>
              <h1 className="mb-6 text-4xl font-bold tracking-tight sm:text-5xl md:text-6xl bg-clip-text text-transparent bg-gradient-to-r from-gray-900 via-gray-800 to-gray-900">
                Analysez vos CV professionnellement avec jesser bou3asba
              </h1>
              <p className="mx-auto mb-8 max-w-2xl text-lg text-gray-600 md:text-xl">
                Notre plateforme utilise l'intelligence artificielle et des critères internationaux pour analyser et
                optimiser votre CV, augmentant significativement vos chances de décrocher l'emploi de vos rêves.
              </p>
              <div className="flex flex-col sm:flex-row gap-4 justify-center">
                <Link href="/register">
                  <Button size="lg" className="rounded-full h-12 px-8 shadow-lg hover:shadow-xl transition-all">
                    Commencer maintenant
                    <ArrowRight className="ml-2 h-4 w-4" />
                  </Button>
                </Link>
                <Link href="#demo">
                  <Button
                    size="lg"
                    variant="outline"
                    className="rounded-full h-12 px-8 border-gray-300 hover:bg-gray-50 transition-all"
                  >
                    Voir une démo
                  </Button>
                </Link>
              </div>
              <div className="mt-8 flex items-center justify-center gap-4 text-sm text-gray-500">
                <div className="flex items-center">
                  <CheckCircle className="mr-1.5 h-4 w-4 text-primary" />
                  Analyse en 2 minutes
                </div>
                <div className="flex items-center">
                  <CheckCircle className="mr-1.5 h-4 w-4 text-primary" />
                  Standards internationaux
                </div>
                <div className="flex items-center">
                  <CheckCircle className="mr-1.5 h-4 w-4 text-primary" />
                  Essai gratuit
                </div>
              </div>
            </div>
          </div>

          {/* Hero Image */}
          <div className="container mt-16 md:mt-24">
            <div className="relative mx-auto max-w-5xl rounded-xl bg-white shadow-2xl overflow-hidden">
              <div className="aspect-[16/9] w-full bg-gray-100 overflow-hidden">
                <img
                  src="/placeholder.svg?height=1080&width=1920"
                  alt="CV Analyzer Dashboard"
                  className="w-full h-full object-cover"
                />
                <div className="absolute inset-0 bg-gradient-to-t from-black/20 to-transparent"></div>
              </div>
              <div className="absolute top-4 left-4 bg-white/90 backdrop-blur-sm rounded-lg px-4 py-2 shadow-lg">
                <div className="flex items-center gap-2">
                  <Badge variant="outline" className="bg-green-50 text-green-700 border-green-200">
                    Score: 92/100
                  </Badge>
                  <Badge variant="outline" className="bg-blue-50 text-blue-700 border-blue-200">
                    Classement: A+
                  </Badge>
                </div>
              </div>
            </div>
          </div>

          {/* Logos des entreprises */}
          <div className="container mt-20">
            <p className="text-center text-sm font-medium text-gray-500 mb-6">
              UTILISÉ PAR LES PROFESSIONNELS DU RECRUTEMENT DANS LE MONDE ENTIER
            </p>
            <div className="mx-auto max-w-5xl grid grid-cols-2 md:grid-cols-6 gap-8 items-center opacity-70">
              <div className="flex justify-center">
                <div className="h-6 w-24 bg-gray-400 rounded"></div>
              </div>
              <div className="flex justify-center">
                <div className="h-6 w-24 bg-gray-400 rounded"></div>
              </div>
              <div className="flex justify-center">
                <div className="h-6 w-24 bg-gray-400 rounded"></div>
              </div>
              <div className="flex justify-center">
                <div className="h-6 w-24 bg-gray-400 rounded"></div>
              </div>
              <div className="flex justify-center">
                <div className="h-6 w-24 bg-gray-400 rounded"></div>
              </div>
              <div className="flex justify-center">
                <div className="h-6 w-24 bg-gray-400 rounded"></div>
              </div>
            </div>
          </div>
        </section>

        {/* Section Statistiques */}
        <section className="py-16 bg-white">
          <div className="container">
            <div className="mx-auto max-w-5xl grid grid-cols-1 md:grid-cols-3 gap-8">
              <div className="flex flex-col items-center text-center p-6 rounded-xl bg-gray-50 border border-gray-100 shadow-sm">
                <div className="mb-4 rounded-full bg-primary/10 p-3">
                  <Target className="h-6 w-6 text-primary" />
                </div>
                <h3 className="text-3xl font-bold mb-2">98%</                <p className="text-gray-600">des utilisateurs améliorent leur CV après notre analyse</p>
              </div>
              <div className="flex flex-col items-center text-center p-6 rounded-xl bg-gray-50 border border-gray-100 shadow-sm">
                <div className="mb-4 rounded-full bg-primary/10 p-3">
                  <Zap className="h-6 w-6 text-primary" />
                </div>
                <h3 className="text-3xl font-bold mb-2">2x</h3>
                <p className="text-gray-600">plus de chances d'être convoqué à un entretien</p>
              </div>
              <div className="flex flex-col items-center text-center p-6 rounded-xl bg-gray-50 border border-gray-100 shadow-sm">
                <div className="mb-4 rounded-full bg-primary/10 p-3">
                  <Globe className="h-6 w-6 text-primary" />
                </div>
                <h3 className="text-3xl font-bold mb-2">25+</h3>
                <p className="text-gray-600">critères internationaux d'évaluation</p>
              </div>
            </div>
          </div>
        </section>

        {/* Section Fonctionnalités */}
        <section id="features" className="py-20 bg-gray-50">
          <div className="container">
            <div className="mx-auto max-w-3xl text-center mb-16">
              <Badge className="mb-4 rounded-full px-4 py-1.5 text-sm font-medium">Fonctionnalités</Badge>
              <h2 className="text-3xl font-bold tracking-tight sm:text-4xl mb-4">Une analyse complète de votre CV</h2>
              <p className="text-lg text-gray-600">
                Notre plateforme utilise des algorithmes avancés et des critères internationaux pour analyser chaque
                aspect de votre CV.
              </p>
            </div>

            <div className="mx-auto max-w-6xl grid grid-cols-1 md:grid-cols-3 gap-8">
              <div className="bg-white rounded-xl p-6 shadow-sm border border-gray-100 hover:shadow-md transition-shadow">
                <div className="mb-4 rounded-full bg-blue-50 p-3 w-fit">
                  <Layers className="h-6 w-6 text-blue-600" />
                </div>
                <h3 className="text-xl font-bold mb-2">Analyse structurelle</h3>
                <p className="text-gray-600">
                  Évaluation de la mise en page, de la lisibilité et de l'organisation générale de votre CV.
                </p>
              </div>
              <div className="bg-white rounded-xl p-6 shadow-sm border border-gray-100 hover:shadow-md transition-shadow">
                <div className="mb-4 rounded-full bg-purple-50 p-3 w-fit">
                  <BarChart className="h-6 w-6 text-purple-600" />
                </div>
                <h3 className="text-xl font-bold mb-2">Analyse de contenu</h3>
                <p className="text-gray-600">
                  Évaluation de vos expériences, compétences et formations selon les standards du marché.
                </p>
              </div>
              <div className="bg-white rounded-xl p-6 shadow-sm border border-gray-100 hover:shadow-md transition-shadow">
                <div className="mb-4 rounded-full bg-amber-50 p-3 w-fit">
                  <Lightbulb className="h-6 w-6 text-amber-600" />
                </div>
                <h3 className="text-xl font-bold mb-2">Recommandations</h3>
                <p className="text-gray-600">Suggestions personnalisées pour améliorer chaque section de votre CV.</p>
              </div>
              <div className="bg-white rounded-xl p-6 shadow-sm border border-gray-100 hover:shadow-md transition-shadow">
                <div className="mb-4 rounded-full bg-green-50 p-3 w-fit">
                  <Award className="h-6 w-6 text-green-600" />
                </div>
                <h3 className="text-xl font-bold mb-2">Classement international</h3>
                <p className="text-gray-600">
                  Évaluation de votre CV selon les standards internationaux avec un score global.
                </p>
              </div>
              <div className="bg-white rounded-xl p-6 shadow-sm border border-gray-100 hover:shadow-md transition-shadow">
                <div className="mb-4 rounded-full bg-red-50 p-3 w-fit">
                  <Target className="h-6 w-6 text-red-600" />
                </div>
                <h3 className="text-xl font-bold mb-2">Analyse ATS</h3>
                <p className="text-gray-600">
                  Vérification de la compatibilité de votre CV avec les systèmes de suivi des candidatures.
                </p>
              </div>
              <div className="bg-white rounded-xl p-6 shadow-sm border border-gray-100 hover:shadow-md transition-shadow">
                <div className="mb-4 rounded-full bg-indigo-50 p-3 w-fit">
                  <Rocket className="h-6 w-6 text-indigo-600" />
                </div>
                <h3 className="text-xl font-bold mb-2">Adéquation au marché</h3>
                <p className="text-gray-600">
                  Analyse de la correspondance entre votre profil et les tendances actuelles du marché.
                </p>
              </div>
            </div>
          </div>
        </section>

        {/* Section Comment ça marche */}
        <section className="py-20 bg-white">
          <div className="container">
            <div className="mx-auto max-w-3xl text-center mb-16">
              <Badge className="mb-4 rounded-full px-4 py-1.5 text-sm font-medium">Processus simple</Badge>
              <h2 className="text-3xl font-bold tracking-tight sm:text-4xl mb-4">Comment ça fonctionne</h2>
              <p className="text-lg text-gray-600">
                Trois étapes simples pour obtenir une analyse professionnelle de votre CV
              </p>
            </div>

            <div className="mx-auto max-w-5xl">
              <div className="grid grid-cols-1 md:grid-cols-3 gap-8">
                <div className="relative flex flex-col items-center text-center">
                  <div className="mb-6 flex h-16 w-16 items-center justify-center rounded-full bg-primary text-white text-2xl font-bold shadow-md">
                    1
                  </div>
                  <h3 className="text-xl font-bold mb-2">Créez un compte</h3>
                  <p className="text-gray-600">
                    Inscrivez-vous en quelques secondes avec votre email ou vos comptes sociaux.
                  </p>

                  {/* Ligne de connexion (visible uniquement sur desktop) */}
                  <div className="absolute top-8 left-[calc(50%+4rem)] w-full h-0.5 bg-gray-200 hidden md:block"></div>
                </div>
                <div className="relative flex flex-col items-center text-center">
                  <div className="mb-6 flex h-16 w-16 items-center justify-center rounded-full bg-primary text-white text-2xl font-bold shadow-md">
                    2
                  </div>
                  <h3 className="text-xl font-bold mb-2">Téléchargez votre CV</h3>
                  <p className="text-gray-600">Importez votre CV au format PDF, DOCX ou autres formats courants.</p>

                  {/* Ligne de connexion (visible uniquement sur desktop) */}
                  <div className="absolute top-8 left-[calc(50%+4rem)] w-full h-0.5 bg-gray-200 hidden md:block"></div>
                </div>
                <div className="flex flex-col items-center text-center">
                  <div className="mb-6 flex h-16 w-16 items-center justify-center rounded-full bg-primary text-white text-2xl font-bold shadow-md">
                    3
                  </div>
                  <h3 className="text-xl font-bold mb-2">Obtenez votre analyse</h3>
                  <p className="text-gray-600">
                    Recevez une analyse détaillée avec un score et des recommandations personnalisées.
                  </p>
                </div>
              </div>

              <div className="mt-16 text-center">
                <Link href="/register">
                  <Button size="lg" className="rounded-full h-12 px-8 shadow-md hover:shadow-lg transition-all">
                    Commencer gratuitement
                    <ArrowRight className="ml-2 h-4 w-4" />
                  </Button>
                </Link>
              </div>
            </div>
          </div>
        </section>

        {/* Section Témoignages */}
        <section id="testimonials" className="py-20 bg-gray-50">
          <div className="container">
            <div className="mx-auto max-w-3xl text-center mb-16">
              <Badge className="mb-4 rounded-full px-4 py-1.5 text-sm font-medium">Témoignages</Badge>
              <h2 className="text-3xl font-bold tracking-tight sm:text-4xl mb-4">Ce que disent nos utilisateurs</h2>
              <p className="text-lg text-gray-600">
                Des milliers de professionnels ont déjà amélioré leur CV grâce à notre plateforme
              </p>
            </div>

            <div className="mx-auto max-w-6xl grid grid-cols-1 md:grid-cols-3 gap-8">
              <div className="bg-white rounded-xl p-6 shadow-sm border border-gray-100">
                <div className="flex items-center mb-4">
                  <div className="flex text-amber-400">
                    <Star className="h-5 w-5 fill-current" />
                    <Star className="h-5 w-5 fill-current" />
                    <Star className="h-5 w-5 fill-current" />
                    <Star className="h-5 w-5 fill-current" />
                    <Star className="h
