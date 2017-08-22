# Maintainer: Eric Vidal <eric@obarun.org>

pkgname=wpa-supplicant-s6rcserv
pkgver=0.1
pkgrel=2
pkgdesc="wpa_supplicant service for"
arch=(x86_64)
license=('beerware')
depends=('wpa_supplicant' 's6' 's6-rc' 's6-boot')
conflicts=()
source=('wpa-supplicant.longrun.dependencies'
		'wpa-supplicant.longrun.pipeline-name'
		'wpa-supplicant.longrun.producer-for'
		'wpa-supplicant.longrun.run'	
		'wpa-supplicant.longrun.type'	
		
		'wpa-supplicant.log.consumer-for'
		'wpa-supplicant.log.dependencies'
		'wpa-supplicant.log.run'
		'wpa-supplicant.log.type'
		
		'bundle.wpa-supplicant.contents'
		'bundle.wpa-supplicant.type'
		'wpa-supplicant.logd'
		'LICENSE')
md5sums=('68b329da9893e34099c7d8ad5cb9c940'
         '5098eaf66263c4feceb893c3df5ccd22'
         '764a3807444891cdd13e2d2b23c57eb2'
         '488689115508887d2fd495e15839c8c6'
         '42c13bdd7f61c06ac59c1aaca9c0f07a'
         '67a8eaa4602345ea09b45ca55e51f5af'
         '68b329da9893e34099c7d8ad5cb9c940'
         'a1fc5f3ef56404b8ec66aa5bad3acc1d'
         '42c13bdd7f61c06ac59c1aaca9c0f07a'
         'b42de0d1c300c7396f516488ab6865c7'
         '71abe97e2554d37f1d12c5bf4945297f'
         'e06abdc3c50265c90227d86921725449'
         '191a37ae657aa17e37e75d0242865dba')

package() {
	
	# bundle , trouble here user-wpa-supplicant need a maj at wpa-supplicant e.g user-Base
	install -Dm 0644 "$srcdir/bundle.wpa-supplicant.contents" "$pkgdir/etc/s6-serv/available/rc/bundle-Wpa-supplicant/contents"
	install -Dm 0644 "$srcdir/bundle.wpa-supplicant.type" "$pkgdir/etc/s6-serv/available/rc/bundle-Wpa-supplicant/type"
	
	# longrun
	install -Dm 0644 "$srcdir/wpa-supplicant.longrun.dependencies" "$pkgdir/etc/s6-serv/available/rc/wpa-supplicant-longrun/dependencies"
	install -Dm 0644 "$srcdir/wpa-supplicant.longrun.pipeline-name" "$pkgdir/etc/s6-serv/available/rc/wpa-supplicant-longrun/pipeline-name"
	install -Dm 0644 "$srcdir/wpa-supplicant.longrun.producer-for" "$pkgdir/etc/s6-serv/available/rc/wpa-supplicant-longrun/producer-for"
	install -Dm 0644 "$srcdir/wpa-supplicant.longrun.run" "$pkgdir/etc/s6-serv/available/rc/wpa-supplicant-longrun/run"
	install -Dm 0644 "$srcdir/wpa-supplicant.longrun.type" "$pkgdir/etc/s6-serv/available/rc/wpa-supplicant-longrun/type"
	
	# log
	install -Dm 0644 "$srcdir/wpa-supplicant.log.consumer-for" "$pkgdir/etc/s6-serv/available/rc/wpa-supplicant-log/consumer-for"
	install -Dm 0644 "$srcdir/wpa-supplicant.log.dependencies" "$pkgdir/etc/s6-serv/available/rc/wpa-supplicant-log/dependencies"
	install -Dm 0644 "$srcdir/wpa-supplicant.log.run" "$pkgdir/etc/s6-serv/available/rc/wpa-supplicant-log/run"
	install -Dm 0644 "$srcdir/wpa-supplicant.log.type" "$pkgdir/etc/s6-serv/available/rc/wpa-supplicant-log/type"
	
	# hook
	install -Dm 0644 "$srcdir/wpa-supplicant.logd" "$pkgdir/etc/s6-serv/log.d/wpa-supplicant-rc"
	
	install -Dm 0644 "$srcdir/LICENSE" "$pkgdir/usr/share/licenses/wpa-supplicant-s6rcserv/LICENSE"
}
