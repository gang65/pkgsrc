# $NetBSD: Makefile,v 1.27 2020/01/18 23:35:59 rillig Exp $
#

DISTNAME=		libXcursor-1.1.2
PKGNAME=		${DISTNAME:S/libX/x/}
PKGREVISION=		2
CATEGORIES=		x11 devel
MASTER_SITES=		https://xlibs.freedesktop.org/release/
EXTRACT_SUFX=		.tar.bz2

MAINTAINER=		pkgsrc-users@NetBSD.org
HOMEPAGE=		https://www.freedesktop.org/Software/xlibs
COMMENT=		Client-side cursor loading library for X

CONFLICTS+=		libXcursor-[0-9]*

USE_TOOLS+=		pkg-config
USE_PKGLOCALEDIR=	yes
USE_LIBTOOL=		yes
GNU_CONFIGURE=		yes

PKGCONFIG_OVERRIDE+=	xcursor.pc.in

BUILDLINK_API_DEPENDS.Xrender+=	Xrender>=0.8

.include "../../x11/libXfixes/buildlink3.mk"
.include "../../x11/libXrender/buildlink3.mk"
.include "../../mk/bsd.pkg.mk"
