# Previous maintainer: Proud Zhu <proudzhu.fdu at gmail dot com>
# Contributor: Lukas Fleischer <archlinux at cryptocrack dot de>
# Contributor: Alexey Yakovenko <waker@users.sourceforge.net>

pkgname=deadbeef-gtk2
_pkgname=deadbeef
pkgver=0.6.0
pkgrel=2
pkgdesc='An audio player for GNU/Linux based on GTK2.'
arch=('i686' 'x86_64')
url='http://deadbeef.sourceforge.net'
license=('GPL2')
depends=('gtk2' 'alsa-lib' 'hicolor-icon-theme' 'desktop-file-utils')
makedepends=('libvorbis' 'libmad' 'flac' 'curl' 'imlib2' 'wavpack' 'libsndfile' 'libcdio' 'libcddb' 'libx11' 'faad2' 'zlib' 'intltool' 'pkgconfig' 'libpulse' 'libzip' 'libsamplerate' 'yasm')
optdepends=('libsamplerate: for Resampler plugin'
            'libvorbis: for Ogg Vorbis playback'
            'libmad: for MP1/MP2/MP3 playback'
            'flac: for FLAC playback'
            'curl: for Last.fm scrobbler, SHOUTcast, Icecast, Podcast support'
            'imlib2: for artwork plugin'
            'wavpack: for WavPack playback'
            'libsndfile: for Wave playback'
            'libcdio: audio cd plugin'
            'libcddb: audio cd plugin'
            'faad2: for AAC/MP4 support'
            'dbus: for OSD notifications support'
            'pulseaudio: for PulseAudio output plugin'
            'libx11: for global hotkeys plugin'
            'zlib: for Audio Overload plugin'
            'libzip: for vfs_zip plugin')
provides=("deadbeef=${pkgver}")
conflicts=('deadbeef')
options=('!libtool')
install='deadbeef-gtk2.install'
source=("http://downloads.sourceforge.net/project/${_pkgname}/${_pkgname}-${pkgver}.tar.bz2")
md5sums=('f1bbb1a0164ed7bcba9c0c8cd1dddcb5')

build() {
  cd "${srcdir}/${_pkgname}-${pkgver}"

  ./configure --prefix=/usr --disable-ffmpeg --enable-gtk2 --disable-gtk3
  make
}

package () {
  cd "${srcdir}/${_pkgname}-${pkgver}"

  make prefix="${pkgdir}/usr" install
}
