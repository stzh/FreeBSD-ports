# $FreeBSD$

PORTNAME=	HHFW-upgrade
PORTVERSION=	0.62
CATEGORIES=	sysutils
MASTER_SITES=	# empty
DISTFILES=	# empty
EXTRACT_ONLY=	# empty

MAINTAINER=	stevenzhou_pmp@163.com
COMMENT=	HHFW upgrade script

LICENSE=	APACHE20

NO_MTREE=	yes
NO_BUILD=	yes

PLIST_FILES=	libexec/HHFW-upgrade \
		sbin/HHFW-upgrade

do-extract:
	@${MKDIR} ${WRKSRC}
	${CP} -r ${FILESDIR}/* ${WRKSRC}

do-install:
	${MKDIR} ${STAGEDIR}${PREFIX}/sbin
	${MKDIR} ${STAGEDIR}${PREFIX}/libexec
	${INSTALL_SCRIPT} ${WRKSRC}/HHFW-upgrade \
		${STAGEDIR}${PREFIX}/libexec
	${INSTALL_SCRIPT} ${WRKSRC}/HHFW-upgrade.wrapper \
		${STAGEDIR}${PREFIX}/sbin/HHFW-upgrade

.include <bsd.port.mk>
