# $FreeBSD$

PORTNAME=	kcalcore
DISTVERSION=	${KDE_APPLICATIONS_VERSION}
CATEGORIES=	net kde kde-applications

MAINTAINER=	kde@FreeBSD.org
COMMENT=	KDE calendar access library

LICENSE=	LGPL21

LIB_DEPENDS=	libical.so:devel/libical

USES=		bison cmake compiler:c++11-lib gettext kde:5 qt:5 tar:xz
USE_KDE=	ecm emoticons init itemmodels itemviews kdelibs4support
USE_QT=		core gui \
		buildtools_build qmake_build
USE_LDCONFIG=	yes

DESCR=		${.CURDIR:H:H}/deskutils/kdepim/pkg-descr


OPTIONS_DEFINE=	DOCS

.include <bsd.port.mk>
