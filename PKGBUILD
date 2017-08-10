# Maintainer: Eric Vidal <eric@obarun.org>

pkgname=wpa-supplicant-s6rcserv
pkgver=0.1
pkgrel=1
pkgdesc="wpa_supplicant service for s6"
arch=(x86_64)
license=('beerware')
depends=('wpa_supplicant' 's6' 's6-rc' 's6-boot')
conflicts=()
install=wpa-supplicant-s6rcserv.install
source=('wpa-supplicant.daemon.dependencies.s6'
		'wpa-supplicant.daemon.pipeline-name.s6'
		'wpa-supplicant.daemon.producer-for.s6'
		'wpa-supplicant.daemon.run.s6'	
		'wpa-supplicant.daemon.type.s6'	
		
		'wpa-supplicant.log.consumer-for.s6'
		'wpa-supplicant.log.dependencies.s6'
		'wpa-supplicant.log.run.s6'
		'wpa-supplicant.log.type.s6'
		
		'bundle.wpa-supplicant.contents.s6'
		'bundle.wpa-supplicant.type.s6'
		'LICENSE')
md5sums=('68b329da9893e34099c7d8ad5cb9c940'
         '5098eaf66263c4feceb893c3df5ccd22'
         '764a3807444891cdd13e2d2b23c57eb2'
         '488689115508887d2fd495e15839c8c6'
         '42c13bdd7f61c06ac59c1aaca9c0f07a'
         '374ac899ff69ad02be2ea47722d407a2'
         '68b329da9893e34099c7d8ad5cb9c940'
         'a1fc5f3ef56404b8ec66aa5bad3acc1d'
         '42c13bdd7f61c06ac59c1aaca9c0f07a'
         '561c501e23561ca591e4bad0d305ae64'
         '71abe97e2554d37f1d12c5bf4945297f'
         '191a37ae657aa17e37e75d0242865dba')

package() {
	
	# bundle , trouble here user-wpa-supplicant need a maj at wpa-supplicant e.g user-Base
	install -Dm 0644 "$srcdir/bundle.wpa-supplicant.contents.s6" "$pkgdir/etc/s6-serv/available/rc/bundle-Wpa-supplicant/contents"
	install -Dm 0644 "$srcdir/bundle.wpa-supplicant.type.s6" "$pkgdir/etc/s6-serv/available/rc/bundle-Wpa-supplicant/type"
	
	# daemon
	install -Dm 0644 "$srcdir/wpa-supplicant.daemon.dependencies.s6" "$pkgdir/etc/s6-serv/available/rc/wpa-supplicant-daemon/dependencies"
	install -Dm 0644 "$srcdir/wpa-supplicant.daemon.pipeline-name.s6" "$pkgdir/etc/s6-serv/available/rc/wpa-supplicant-daemon/pipeline-name"
	install -Dm 0644 "$srcdir/wpa-supplicant.daemon.producer-for.s6" "$pkgdir/etc/s6-serv/available/rc/wpa-supplicant-daemon/producer-for"
	install -Dm 0644 "$srcdir/wpa-supplicant.daemon.run.s6" "$pkgdir/etc/s6-serv/available/rc/wpa-supplicant-daemon/run"
	install -Dm 0644 "$srcdir/wpa-supplicant.daemon.type.s6" "$pkgdir/etc/s6-serv/available/rc/wpa-supplicant-daemon/type"
	
	# log
	install -Dm 0644 "$srcdir/wpa-supplicant.log.consumer-for.s6" "$pkgdir/etc/s6-serv/available/rc/wpa-supplicant-log/consumer-for"
	install -Dm 0644 "$srcdir/wpa-supplicant.log.dependencies.s6" "$pkgdir/etc/s6-serv/available/rc/wpa-supplicant-log/dependencies"
	install -Dm 0644 "$srcdir/wpa-supplicant.log.run.s6" "$pkgdir/etc/s6-serv/available/rc/wpa-supplicant-log/run"
	install -Dm 0644 "$srcdir/wpa-supplicant.log.type.s6" "$pkgdir/etc/s6-serv/available/rc/wpa-supplicant-log/type"
	
	install -Dm 0644 "$srcdir/LICENSE" "$pkgdir/usr/share/licenses/wpa-supplicant-s6rcserv/LICENSE"
}
