# Created by: David Yeske <dyeske@gmail.com>
# $FreeBSD$

PORTNAME=	reallyslick
PORTVERSION=	0.9.1
PORTREVISION=	20
CATEGORIES=	graphics
MASTER_SITES=	SF/rss-glx/rss-glx/${PORTVERSION}
DISTNAME=	rss-glx_${PORTVERSION}

MAINTAINER=	ports@FreeBSD.org
COMMENT=	OpenGL screensaver collection

BROKEN_armv6=		fails to compile: hyperspace.cpp:387:19: non-constant-expression cannot be narrowed from type 'double' to 'float' in initializer list
BROKEN_armv7=		fails to compile: hyperspace.cpp:387:19: non-constant-expression cannot be narrowed from type 'double' to 'float' in initializer list

LIB_DEPENDS=	libMagickWand-6.so:graphics/ImageMagick \
		libGLC.so:graphics/quesoglc

USES=		gmake pathfix pkgconfig tar:bzip2 libtool
USE_GL=		glut
GNU_CONFIGURE=	yes

CPPFLAGS+=	-I${LOCALBASE}/include
LIBS+=		-L${LOCALBASE}/lib -lXext

OPTIONS_DEFINE=	FREEALUT GLEW

FREEALUT_DESC=	Enable freealut support
FREEALUT_CONFIGURE_ENABLE=	sound
FREEALUT_USES=	openal:alut

GLEW_DESC=	Enable GLEW support
GLEW_USE=	GL=glew
GLEW_CONFIGURE_ENV_OFF=	ac_cv_header_GL_glew_h=no

post-patch:
	@${REINPLACE_CMD} '/LINK.*pixelcity/s/LINK/CXXLINK/' ${WRKSRC}/src/Makefile.in

.include <bsd.port.mk>
