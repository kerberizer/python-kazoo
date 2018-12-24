# Maintainer: Luchesar V. ILIEV <luchesar.iliev@gmail.com>

pkgbase='python-kazoo'

pkgname=(
    'python-kazoo'
    'python2-kazoo'
)

pkgver=2.6.0
pkgrel=1

pkgdesc='High-level Python library for Apache Zookeeper'
arch=('any')
url='https://kazoo.readthedocs.io/'
license=('Apache')

makedepends=(
    'python'
    'python-setuptools'
    'python-six'
    'python2'
    'python2-setuptools'
    'python2-six'
)

_name='kazoo'
_pypi='files.pythonhosted.org/packages/source'

source=(
    "https://${_pypi}/${_name::1}/${_name}/${_name}-${pkgver}.tar.gz"
)

sha512sums=(
    '0f6c2def5a1256f9c7ce80e7c6701adf4f0998876b17aa767525566f6de07044573d7b47f1ddd122c5705744f2c1af35ab4a4dc1d103ffc245e3f576c209436a'
)

build() {
    cd "${srcdir}/${_name}-${pkgver}"
    python setup.py build
}

package_python-kazoo() {
    depends=(
        'python'
        'python-six'
    )
    cd "${srcdir}/${_name}-${pkgver}"
    python setup.py install --root="${pkgdir}/" --optimize=1 --skip-build
}

package_python2-kazoo() {
    depends=(
        'python2'
        'python2-six'
    )
    cd "${srcdir}/${_name}-${pkgver}"
    python2 setup.py install --root="${pkgdir}/" --optimize=1 --skip-build
}

# vim:set ts=4 sts=4 sw=4 tw=100 et ft=sh:
