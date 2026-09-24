<script setup>
import hero from './assets/hero.jpg'
import misionArt from './assets/mision-art.png'
import vidas from './assets/vidas.png'
import milo from './assets/milo.jpg'
import luna from './assets/luna.jpg'

const navLinks = ['Inicio', 'Cómo funciona', 'Plataforma', 'FAQ', 'Contacto']
const features = ['Crear nuevas prótesis', 'Gestionar diseños', 'Historial y versiones', 'Exportar modelos 3D']
</script>

<template>
  <div class="min-h-screen overflow-x-hidden font-sans text-white">
    <!-- ================= HERO ================= -->
    <section
      id="inicio"
      class="relative h-171 bg-cover bg-center"
      :style="{ backgroundImage: `url(${hero})` }"
    >
      <div class="relative mx-auto h-full max-w-360">
        <!-- Navbar -->
        <header class="absolute inset-x-0 top-0 flex items-start">
          <a href="#" class="absolute left-10.75 top-7.5 font-display text-[31px] font-bold tracking-[-0.04em]">hunda.</a>

          <nav class="absolute left-95.75 top-8.75 hidden items-center gap-8.25 text-[15px] font-medium md:flex">
            <a
              v-for="(link, i) in navLinks"
              :key="link"
              href="#"
              class="relative pb-1.5"
            >
              {{ link }}
              <span v-if="i === 0" class="absolute inset-x-0 -bottom-0.5 h-[1.5px] rounded bg-mint"></span>
            </a>
          </nav>

          <a href="#" class="absolute left-269.25 top-11.25 hidden text-[15px] text-white/90 lg:block">Iniciar Sesion</a>
          <a
            href="#"
            class="absolute right-10.75 top-6.75 flex h-14 w-44 items-center justify-center gap-6 rounded-full bg-linear-to-b from-[#1ef0a5] to-[#8ff7cf] text-[14px] font-medium text-[#0d2a20] shadow-[0_6px_22px_rgba(0,227,154,0.45)]"
          >
            Crear usuario
            <svg class="h-3.5 w-3.5" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.4" stroke-linecap="round" stroke-linejoin="round">
              <path d="M5 12h14M13 6l6 6-6 6" />
            </svg>
          </a>
        </header>

        <!-- Hero content -->
        <div class="absolute left-23.5 top-41.5">
          <p class="text-[15px] font-medium uppercase tracking-[0.34em] text-white/95">Que ninguna huella se detenga</p>
          <h1 class="mt-1.5 font-display text-[55.5px] font-semibold leading-16 tracking-[-0.045em]">
            Por una vida<br />
            animal <span class="text-leaf">sin límites.</span>
          </h1>
          <p class="mt-3.5 text-[19.5px] leading-6 text-white">
            Diseñá prótesis personalizadas a través<br />
            de nuestra plataforma digital y fabricación 3D.
          </p>
        </div>

        <div class="absolute left-22 top-120.5 flex gap-5.75">
          <a href="#" class="flex h-15 w-70.75 items-center justify-center rounded-full bg-mint text-[16px] font-medium text-[#0d2a20]">
            Crear mi prótesis
          </a>
          <a
            href="#"
            class="flex h-15 w-60.75 items-center justify-center rounded-full border border-white/10 bg-[#3d4a2b]/55 text-[16px] text-white/70 backdrop-blur-sm"
          >
            Ver demo
          </a>
        </div>

        <ul class="absolute left-24.25 top-144 flex items-center gap-10 text-[15.5px] text-white">
          <li class="flex items-center gap-2.5">
            <svg class="h-6 w-6" viewBox="0 0 24 24">
              <circle cx="12" cy="12" r="11" fill="#1fbf7c" opacity=".35" />
              <path d="M12 18s-5.5-3.4-5.5-7.1A3 3 0 0 1 12 9.2a3 3 0 0 1 5.5 1.7C17.5 14.6 12 18 12 18z" fill="#22d88f" />
              <circle cx="9.5" cy="11.5" r=".9" fill="#0d2a20" /><circle cx="14.5" cy="11.5" r=".9" fill="#0d2a20" />
            </svg>
            Personalizadas
          </li>
          <li class="flex items-center gap-2.5">
            <svg class="h-6.5 w-6.5" viewBox="0 0 24 24" fill="none" stroke="#22d88f" stroke-width="1.8">
              <circle cx="12" cy="12" r="8" /><circle cx="12" cy="12" r="3" fill="#22d88f" opacity=".4" />
              <path d="M12 2v5M12 17v5M2 12h5M17 12h5" />
            </svg>
            Precisas
          </li>
          <li class="flex items-center gap-2.5">
            <svg class="h-6.5 w-6.5" viewBox="0 0 24 24" fill="none" stroke="#22d88f" stroke-width="1.6">
              <circle cx="12" cy="12" r="10" />
              <path d="M14.8 9.2c-.4-1-1.5-1.7-2.8-1.7-1.6 0-2.8.9-2.8 2.2 0 3 5.6 1.5 5.6 4.5 0 1.3-1.2 2.3-2.8 2.3-1.4 0-2.5-.7-2.9-1.8M12 6v1.5M12 16.5V18" />
            </svg>
            Accesibles
          </li>
        </ul>
      </div>
    </section>

    <!-- ================= MISIÓN ================= -->
    <section class="relative h-127.5 bg-[linear-gradient(90deg,#2d4741_0%,#334845_55%,#374647_100%)]">
      <div class="dots absolute inset-0"></div>
      <div class="relative mx-auto h-full max-w-360">
        <img
          :src="misionArt"
          alt=""
          class="absolute left-0 top-7.5 w-190 select-none mask-[linear-gradient(to_left,transparent,black_3%),linear-gradient(to_bottom,transparent,black_4%,black_96%,transparent)] mask-intersect"
        />

        <div class="absolute left-199.25 top-27">
          <p class="text-[14px] font-medium uppercase text-white/95">Nuestra misión</p>
          <h2 class="mt-2.5 font-display text-[40px] font-semibold leading-12.75 tracking-[0.01em]">
            Tecnología<br />
            al servicio de <span class="text-leaf">su bienestar.</span>
          </h2>
          <p class="mt-1 text-[19.6px] leading-6 text-white">
            Creemos en un futuro donde todos los animales<br />
            tengan &nbsp;la oportunidad de moverse, explorar y<br />
            disfrutar sin limitaciones.
          </p>
          <a
            href="#"
            class="mt-8.75 -ml-1.5 flex h-15 w-78.75 items-center justify-center rounded-full bg-mint text-[14.5px] font-semibold text-[#0d2a20] shadow-[0_8px_26px_rgba(0,227,154,0.3)]"
          >
            Conocé más sobre hunda
          </a>
        </div>

        <img :src="vidas" alt="" class="absolute left-308.25 top-88.75 w-46 select-none mask-[linear-gradient(to_right,transparent,black_12px,black_calc(100%-12px),transparent),linear-gradient(to_bottom,transparent,black_12px,black_calc(100%-12px),transparent)] mask-intersect" />
      </div>
    </section>

    <!-- ================= PLATAFORMA ================= -->
    <section
      id="plataforma"
      class="relative h-165 border-t border-white/10 bg-[linear-gradient(180deg,#545b5d_0%,#625c67_45%,#5f5a64_75%,#57555d_100%)]"
    >
      <div class="dots absolute inset-0 opacity-70"></div>
      <div class="relative mx-auto h-full max-w-360">
        <!-- Left copy -->
        <div class="absolute left-23 top-16">
          <p class="ml-0.75 text-[14px] font-medium uppercase text-white/95">La plataforma</p>
          <h2 class="mt-1.5 font-display text-[39px] font-bold leading-11 tracking-[-0.06em]">
            Controlá todo<br />
            desde un <span class="text-leaf">único lugar.</span>
          </h2>
          <p class="mt-4.5 ml-0.5 text-[17.6px] leading-5.5">
            Diseñá, guardá y hacé seguimiento<br />
            de todas tus prótesis en tu dashboard<br />
            personal.
          </p>
          <ul class="mt-11 ml-2 space-y-3.5 text-[17px]">
            <li v-for="f in features" :key="f" class="flex h-6 items-center gap-2.5">
              <svg class="h-5.5 w-6" viewBox="0 0 24 24" fill="none" stroke="#22d88f" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round">
                <path d="M3 12h17M14 6l6 6-6 6" />
              </svg>
              {{ f }}
            </li>
          </ul>
          <a
            href="#"
            class="mt-10 -ml-1.5 flex h-15 w-70.75 items-center justify-center rounded-full bg-mint text-[15px] font-medium text-[#0d2a20] shadow-[0_8px_26px_rgba(0,227,154,0.35)]"
          >
            Ir a la plataforma
          </a>
        </div>

        <!-- Dashboard mock -->
        <div
          class="absolute left-129.75 top-15.5 h-136.75 w-206.5 overflow-hidden rounded-[10px] border border-white/35 bg-[linear-gradient(180deg,#5e4a5e_0%,#5a5260_45%,#4c5a57_78%,#3e5a50_100%)] shadow-[0_10px_40px_rgba(0,0,0,0.25)]"
        >
          <div class="dots absolute inset-0 opacity-50"></div>
          <div class="relative h-full font-display">
            <h3 class="absolute left-6.25 top-5.5 text-[20px] font-medium">Mis perros</h3>
            <p class="absolute left-6 top-13.75 text-[11px] font-medium text-white/90">Administrá a tus compañeros y sus prótesis</p>
            <a
              href="#"
              class="absolute left-155.25 top-13.25 flex h-9 w-43.5 items-center justify-center rounded-xs bg-[#00f5a0] text-[11px] font-semibold text-[#0d2a20] shadow-[0_4px_14px_rgba(0,245,160,0.3)]"
            >
              + Agregar perro
            </a>

            <!-- Milo -->
            <div class="absolute left-6.25 top-26.75 h-41.75 w-192.5 rounded-md bg-white/9">
              <img :src="milo" alt="Milo" class="absolute left-3 top-3.75 h-34.25 w-34 rounded-[5px] object-cover" />
              <p class="absolute left-43.25 top-5.75 text-[16px] font-medium">Milo</p>
              <p class="absolute left-43 top-13.25 text-[11.5px] text-white/45">Golden Retriever • 6 años</p>
              <div class="absolute left-43 top-20.25 h-px w-79.5 bg-white/60"></div>
              <span class="absolute left-43.5 top-24.5 h-7.5 w-7.5 rounded-full bg-[#d9d9d9]"></span>
              <p class="absolute left-53.75 top-25.25 text-[11px] font-semibold">Prótesis delantera izquierda</p>
              <p class="absolute left-53.75 top-29.75 text-[11px] text-white/50">Tipo: Adaptativa</p>
              <span class="absolute left-99.25 top-26 flex h-6.5 w-19.5 items-center justify-center rounded-[3px] border border-white/10 bg-[#2a1f1d] text-[9px] font-semibold text-[#f5b52a]">
                En proceso
              </span>
              <a href="#" class="absolute left-166 top-18.5 flex items-center gap-5.5 text-[10.5px] font-semibold text-leaf">
                Ver perfil
                <svg class="h-4 w-4 text-white" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.6" stroke-linecap="round" stroke-linejoin="round"><path d="M9 5l7 7-7 7" /></svg>
              </a>
            </div>

            <!-- Luna -->
            <div class="absolute left-6.25 top-73.25 h-41.75 w-192.5 rounded-md bg-white/9">
              <img :src="luna" alt="Luna" class="absolute left-3 top-3.75 h-34.25 w-34 rounded-[5px] object-cover" />
              <p class="absolute left-43.25 top-5.75 text-[16px] font-medium">Luna</p>
              <p class="absolute left-43 top-13.25 text-[11.5px] text-white/45">West Highland White Terrier • &nbsp;4 años</p>
              <div class="absolute left-43 top-20.25 h-px w-79.5 bg-white/60"></div>
              <span class="absolute left-43.5 top-24.5 h-7.5 w-7.5 rounded-full bg-[#d9d9d9]"></span>
              <p class="absolute left-53.75 top-25.25 text-[11px] font-semibold">Sin prótesis activa</p>
              <p class="absolute left-53.75 top-29.75 text-[11px] text-white/50">Todo en orden</p>
              <a href="#" class="absolute left-166 top-18.5 flex items-center gap-5.5 text-[10.5px] font-semibold text-leaf">
                Ver perfil
                <svg class="h-4 w-4 text-white" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.6" stroke-linecap="round" stroke-linejoin="round"><path d="M9 5l7 7-7 7" /></svg>
              </a>
            </div>

            <p class="absolute inset-x-0 top-128.25 flex items-center justify-center gap-2 text-[11px] text-white/55">
              <svg class="h-3.75 w-3.75" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8"><circle cx="12" cy="12" r="10" /><path d="M9.5 9.5a2.5 2.5 0 1 1 3.5 2.3c-.6.3-1 .9-1 1.6v.6M12 17.5h.01" stroke-linecap="round" /></svg>
              ¿Tenés dudas sobre las prótesis de tu perro?
              <a href="#" class="ml-3.5 font-semibold text-leaf">Contactanos</a>
            </p>
          </div>
        </div>
      </div>
    </section>

    <!-- ================= HISTORIAS ================= -->
    <section
      class="relative h-122.5 border-t border-white/10 bg-[radial-gradient(ellipse_at_75%_15%,#4a3a4d_0%,transparent_55%),linear-gradient(160deg,#3b3a44_0%,#3a3844_40%,#393341_70%,#2f3b3b_100%)]"
    >
      <div class="absolute inset-0 bg-[linear-gradient(20deg,rgba(55,80,75,0.55)_0%,transparent_45%)]"></div>
      <div class="dots absolute inset-0 opacity-80"></div>
      <div class="relative mx-auto h-full max-w-360">
        <div class="absolute left-25.25 top-30.5">
          <p class="text-[15px] font-medium uppercase tracking-[0.14em] text-white/95">Historias reales</p>
          <h2 class="mt-2 font-display text-[40.5px] font-semibold leading-11.5 tracking-tighter">
            Ellos ya están<br />
            viviendo <span class="text-leaf">sin límites.</span>
          </h2>
          <p class="mt-4.5 text-[17.5px] leading-5.75 tracking-[0.03em] text-white/95">
            Cada prótesis es una nueva oportunidad<br />
            para seguir explorando el mundo..
          </p>
          <a
            href="#"
            class="mt-10 flex h-15 w-56.75 items-center justify-center rounded-full border border-leaf text-[16px] font-medium text-leaf"
          >
            Ver más historias
          </a>
        </div>

        <button class="absolute left-123.5 top-58.75 h-11 w-11 rounded-full bg-white/15" aria-label="Anterior"></button>
        <button class="absolute left-340.5 top-58.75 h-11 w-11 rounded-full bg-white/15" aria-label="Siguiente"></button>

        <div class="absolute left-228.25 top-110.25 flex items-center gap-0.75">
          <span class="h-3 w-5.75 rounded-full bg-mint"></span>
          <span class="h-3 w-3 rounded-full bg-mint"></span>
          <span class="h-3 w-3 rounded-full bg-mint"></span>
        </div>
      </div>
    </section>

    <!-- ================= SOBRE NOSOTROS + CTA ================= -->
    <section class="relative bg-[#2c443f]">
      <div class="dots absolute inset-0"></div>

      <div class="relative h-126.25 border-t border-white/10 bg-[linear-gradient(90deg,rgba(255,255,255,0.08)_0%,rgba(255,255,255,0.04)_40%,rgba(255,255,255,0.02)_100%)]">
        <div class="relative mx-auto h-full max-w-360">
          <div class="absolute left-20 top-18.5">
            <p class="text-[16px] font-medium uppercase text-white/95">Sobre nosotros</p>
            <h2 class="mt-2 font-display text-[39.5px] font-bold leading-12 tracking-[-0.065em]">
              Somos <span class="text-leaf">Benja, Brigitte y Mayte</span>
            </h2>
            <p class="mt-4.5 text-[17.8px] leading-5.5">
              Estudiantes de ORT TIC apasionados por la<br />
              tecnología, el diseño y el bienestar animal.
            </p>
            <p class="mt-6.25 text-[17.8px] leading-5.5">
              Nuestro objetivo es hacer más accesibles las<br />
              prótesis personalizadas para mejorar la calidad<br />
              de vida de los perros.
            </p>
            <div class="mt-12.5 ml-2.5 flex gap-5.5">
              <a
                href="#"
                class="flex h-15 w-70.75 items-center justify-center rounded-full bg-mint text-[16px] font-medium text-[#0d2a20] shadow-[0_10px_26px_rgba(0,0,0,0.3)]"
              >
                Unite al equipo
              </a>
              <a
                href="#"
                class="flex h-15 w-66.25 items-center justify-center rounded-full border border-leaf text-[15.5px] font-medium text-leaf"
              >
                ¡Conocé más sobre nosotros!
              </a>
            </div>
          </div>
        </div>
      </div>

      <div class="relative h-110">
        <div class="relative mx-auto h-full max-w-360">
          <div class="absolute left-5.25 right-4.25 top-28.75 h-60 rounded-lg bg-white/8.5">
            <div class="absolute left-108.5 top-12">
              <h2 class="font-display text-[55px] font-bold leading-15.5 tracking-[-0.06em]">
                ¿Listo para <span class="text-leaf">comenzar?</span>
              </h2>
              <p class="mt-3 text-[20.3px] leading-6">
                Creá tu cuenta gratis y empezá a diseñar<br />
                la prótesis que tu perro necesita.
              </p>
            </div>
            <a
              href="#"
              class="absolute left-266.75 top-18.25 flex h-13.75 w-66.5 items-center justify-center rounded-full bg-mint text-[16px] font-medium text-[#0d2a20]"
            >
              Crear cuenta
            </a>
            <p class="absolute left-271.75 top-39.5 text-[15px] text-white/90">
              ¿Ya tenes cuenta? <a href="#" class="text-leaf underline underline-offset-2">Iniciá sesión</a>
            </p>
          </div>
        </div>
      </div>
    </section>

    <!-- ================= FOOTER ================= -->
    <footer id="contacto" class="relative h-69.5 bg-[#040a0b]">
      <div class="relative mx-auto h-full max-w-360 tracking-[-0.02em]">
        <div class="absolute left-27.25 top-17">
          <p class="ml-1.25 font-display text-[33px] font-bold tracking-[-0.04em]">hunda.</p>
          <p class="mt-0.75 text-[16px] leading-5.5">
            Innovación, bienestar y movimiento<br />
            para perros
          </p>
        </div>

        <div class="absolute left-135 top-14.5">
          <h4 class="text-[14.5px] font-semibold">NAVEGACIÓN</h4>
          <ul class="mt-4.25 space-y-1.25 text-[14px]">
            <li v-for="l in navLinks" :key="l"><a href="#">{{ l }}</a></li>
          </ul>
        </div>

        <div class="absolute left-204.5 top-14.75">
          <h4 class="text-[14.5px] font-semibold">LEGAL</h4>
          <ul class="mt-4.25 space-y-1.25 text-[14px]">
            <li><a href="#">Términos y condiciones</a></li>
            <li><a href="#">Política de privacidad</a></li>
          </ul>
        </div>

        <div class="absolute left-279.25 top-14.75">
          <h4 class="text-[14.5px] font-semibold">CONTACTO</h4>
          <ul class="mt-4.25 space-y-1.25 text-[14px]">
            <li>betterbm26@gmail.com</li>
            <li>+54 9 11 7366 7824</li>
          </ul>
          <a href="#" class="mt-3.75 block w-fit" aria-label="Instagram">
            <svg class="h-8.5 w-8.5" viewBox="0 0 24 24" fill="none" stroke="white" stroke-width="2">
              <rect x="3" y="3" width="18" height="18" rx="5" />
              <circle cx="12" cy="12" r="4" />
              <circle cx="17.3" cy="6.7" r="1" fill="white" stroke="none" />
            </svg>
          </a>
        </div>

        <p class="absolute right-4.75 top-62.5 text-[14px]">© 2026 hunda. - Todos los derechos reservados</p>
      </div>
    </footer>
  </div>
</template>
