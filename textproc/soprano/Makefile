# Created by: arved
# $FreeBSD$

PORTNAME=	soprano
PORTVERSION=	2.9.4
PORTREVISION=	2
CATEGORIES=	textproc
MASTER_SITES=	SF/${PORTNAME}/Soprano/${PORTVERSION}

MAINTAINER=	kde@FreeBSD.org
COMMENT=	Qt/C++ RDF framework

DEPRECATED=		Qt4 has been EOL since december 2015
EXPIRATION_DATE=	2019-03-15

LIB_DEPENDS=	libraptor2.so:textproc/raptor2 \
		librdf.so:textproc/redland \
		libiodbc.so:databases/libiodbc

USE_QT=		corelib dbus network qtestlib_build xml \
		qmake_build moc_build uic_build rcc_build
USES=		cmake pkgconfig qt:4 tar:bzip2
CMAKE_ARGS+=	-DSOPRANO_DISABLE_CLUCENE_INDEX=yes \
		-DSOPRANO_DISABLE_SESAME2_BACKEND=yes
USE_LDCONFIG=	yes

post-patch:
	@${REINPLACE_CMD} -e 's,$${LIB_SUFFIX}/pkgconfig,data/pkgconfig,' \
		${WRKSRC}/CMakeLists.txt
	@${REINPLACE_CMD} -e 's,soprano/cmake,cmake/Modules,' \
		${WRKSRC}/cmake/modules/CMakeLists.txt

.include <bsd.port.mk>
