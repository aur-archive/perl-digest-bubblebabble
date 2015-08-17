# Contributor: John D Jones III <j[nospace]n[nospace]b[nospace]e[nospace]k[nospace]1972 -_AT_- the domain name google offers a mail service at ending in dot com>
# Generator  : CPANPLUS::Dist::Arch 1.25

pkgname='perl-digest-bubblebabble'
pkgver='0.02'
pkgrel='1'
pkgdesc="Create bubble-babble fingerprints"
arch=('any')
license=('PerlArtistic' 'GPL')
options=('!emptydirs')
depends=('perl>=5.8.1')
makedepends=()
url='http://search.cpan.org/dist/Digest-BubbleBabble'
source=('http://search.cpan.org/CPAN/authors/id/B/BT/BTROTT/Digest-BubbleBabble-0.02.tar.gz')
md5sums=('4d7edd5b0a904db8194aa660d502fbe0')
sha512sums=('7f5d7519184eed07e3b3ce302b7dd10980acf34af91f7ec8a317c2b7faf4a8a35dd4dadecf643c611456554ae7bfa82699afd80af195e801502047b243653ed5')
_distdir="Digest-BubbleBabble-0.02"

build() {
  ( export PERL_MM_USE_DEFAULT=1 PERL5LIB=""                 \
      PERL_AUTOINSTALL=--skipdeps                            \
      PERL_MM_OPT="INSTALLDIRS=vendor DESTDIR='$pkgdir'"     \
      PERL_MB_OPT="--installdirs vendor --destdir '$pkgdir'" \
      MODULEBUILDRC=/dev/null

    cd "$srcdir/$_distdir"
    /usr/bin/perl Makefile.PL
    make
  )
}

check() {
  cd "$srcdir/$_distdir"
  ( export PERL_MM_USE_DEFAULT=1 PERL5LIB=""
    make test
  )
}

package() {
  cd "$srcdir/$_distdir"
  make install

  find "$pkgdir" -name .packlist -o -name perllocal.pod -delete
}

# Local Variables:
# mode: shell-script
# sh-basic-offset: 2
# End:
# vim:set ts=2 sw=2 et:
