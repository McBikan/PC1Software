# PC1Software

# Correr el Bundler

## Preguntas

## ¿Cuál es la diferencia entre el propósito y el contenido de Gemfile y Gemfile.lock? ¿Qué archivo se necesita para reproducir completamente las gemas del entorno de desarrollo en el entorno de producción? Después de ejecutar el bundle, ¿por qué aparecen gemas en Gemfile.lock que no estaban en Gemfile?

### Gemfile
Propósito: Es un archivo donde especificamos todas las gemas que nuestra aplicación necesitará para funcionar correctamente. Son las gemas en las que tu confías, ya sea por su funcionalidad o uso.
Contenido: 

source 'https://rubygems.org'

ruby '2.6.6'

gem 'sinatra', '>= 2.0.1'

end

### Gemlock
Propósito: Es un archivo generado automáticamente después de ejecutar bundle install o bundle update. Su propósito principal es registrar las versiones específicas de las gemas y sus dependencias que se instalaron en el entorno local. Esto garantiza que las mismas versiones de las gemas se utilicen en todos los entornos (desarrollo, prueba, producción) y en diferentes máquinas, lo que evita problemas de inconsistencia.

Contenido: 
GEM
  remote: https://rubygems.org/
  specs:
    ffi (1.16.2-x64-mingw32)
    listen (3.8.0)
      rb-fsevent (~> 0.10, >= 0.10.3)
      rb-inotify (~> 0.9, >= 0.9.10)
    mustermann (3.0.0)
      ruby2_keywords (~> 0.0.1)
    rack (2.2.8)
    rack-protection (3.1.0)
      rack (~> 2.2, >= 2.2.4)
    rb-fsevent (0.11.2)
    rb-inotify (0.10.1)
      ffi (~> 1.0)
    rerun (0.14.0)
      listen (~> 3.0)
    ruby2_keywords (0.0.5)
    sinatra (3.1.0)
      mustermann (~> 3.0)
      rack (~> 2.2, >= 2.2.4)
      rack-protection (= 3.1.0)
      tilt (~> 2.0)
    tilt (2.3.0)

PLATFORMS
  x64-mingw32

DEPENDENCIES
  rerun
  sinatra (>= 2.0.1)

RUBY VERSION
   ruby 2.6.6p146

BUNDLED WITH
   1.17.2

## Preguntas

## ¿Qué sucede si intentas visitar una URL no raíz cómo https://localhost:3000/hello y por qué? (la raíz de tu URL variará)
