# Created by: Alexander Nusov <alexander.nusov@nfvexpress.com>
# $FreeBSD$

PORTNAME=	cliff
PORTVERSION=	2.4.0
CATEGORIES=	devel python
MASTER_SITES=	CHEESESHOP
PKGNAMEPREFIX=	${PYTHON_PKGNAMEPREFIX}

MAINTAINER=	alexander.nusov@nfvexpress.com
COMMENT=	Command Line Interface Formulation Framework

LICENSE=	APACHE20

BUILD_DEPENDS=	${PYTHON_PKGNAMEPREFIX}pbr>=1.6:devel/py-pbr@${FLAVOR}
RUN_DEPENDS=	${PYTHON_PKGNAMEPREFIX}cmd2>=0.6.7:devel/py-cmd2@${FLAVOR} \
		${PYTHON_PKGNAMEPREFIX}prettytable>=0:devel/py-prettytable@${FLAVOR} \
		${PYTHON_PKGNAMEPREFIX}unicodecsv>=0.8.0:devel/py-unicodecsv@${FLAVOR} \
		${PYTHON_PKGNAMEPREFIX}six>=1.9.0:devel/py-six@${FLAVOR} \
		${PYTHON_PKGNAMEPREFIX}stevedore>=1.17.1:devel/py-stevedore@${FLAVOR} \
		${PYTHON_PKGNAMEPREFIX}yaml>=3.10.0:devel/py-yaml@${FLAVOR} \
		${PYTHON_PKGNAMEPREFIX}pyparsing>=2.0.7:devel/py-pyparsing@${FLAVOR}

NO_ARCH=	yes

USES=		python
USE_PYTHON=	autoplist distutils

.include <bsd.port.mk>
