# Contributor: Alexsandr Pavlov <kidoz at mail dot ru>
pkgname=ruby-linecache19
_gemname=${pkgname#ruby-}
pkgver=0.5.13
pkgrel=2
pkgdesc="Linecache is a module for reading and caching lines."
arch=('i686' 'x86_64')
url="http://rubyforge.org/projects/ruby-debug19"
license=('MIT')
depends=('ruby' 'rubygems' 'ruby-ruby_core_source' 'ruby-source')
source=(http://rubyforge.org/frs/download.php/75414/${_gemname}-${pkgver}.gem)
noextract=(${_gemname}-${pkgver}.gem)
md5sums=('744fb0d2e0d7162d098ed7dacaf4a9ab')

build() {
  cd "${srcdir}"
  export HOME=/tmp
  local _gemdir="$(ruby -rubygems -e'puts Gem.default_dir')"
  gem install --no-user-install --ignore-dependencies -i "${pkgdir}${_gemdir}" ${_gemname}-${pkgver}.gem -- --with-ruby-include=/usr/src/ruby-1.9.3-p194
}
