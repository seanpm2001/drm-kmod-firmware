# $FreeBSD$

_VALID_I915KMODS=skylake broxton kabylake geminilake cannonlake \
	icelake elkhartlake tigerlake rocketlake alderlake meteorlake \
	dg1 dg2

I915KMODS?=	${_VALID_I915KMODS}

.for var in ${I915KMODS}
.if empty(_VALID_I915KMODS:M${var})
_INVALID_I915_KMODS+=	${var}
.endif
.endfor
.if !empty(_INVALID_I915_KMODS)
.error "${_INVALID_I915_KMODS} firmware doesn't exists"
.endif

.if ${I915KMODS:Mskylake}
SUBDIR+=	skldmc_127 \
		sklguc_933 \
		sklguc_3300 \
		sklguc_6200 \
		sklhuc_107 \
		sklhuc_200
.endif

.if ${I915KMODS:Mbroxton}
SUBDIR+=	bxtdmc_107 \
		bxtguc_929 \
		bxtguc_3300 \
		bxtguc_6200 \
		bxthuc_107 \
		bxthuc_200
.endif

.if ${I915KMODS:Mkabylake}
SUBDIR+=	kbldmc_104 \
		kblguc_939 \
		kblguc_3300 \
		kblguc_6200 \
		kblhuc_200 \
		kblhuc_400 \
		cmlguc_3300 \
		cmlguc_6200 \
		cmlguc_7011 \
		cmlhuc_400
.endif

.if ${I915KMODS:Mgeminilake}
SUBDIR+=	glkdmc_104 \
		glkguc_3300 \
		glkguc_6200 \
		glkhuc_301 \
		glkhuc_400
.endif

.if ${I915KMODS:Mcannonlake}
SUBDIR+=	cnldmc_106 \
		cnldmc_107
.endif

.if ${I915KMODS:Micelake}
SUBDIR+=	icldmc_107 \
		icldmc_109 \
		iclguc_3300 \
		iclguc_6200 \
		iclhuc_84 \
		iclhuc_900
.endif

.if ${I915KMODS:Melkhartlake}
SUBDIR+=	ehlguc_3304 \
		ehlguc_6200 \
		ehlhuc_900
.endif

.if ${I915KMODS:Mtigerlake}
SUBDIR+=	tgldmc_204 \
		tgldmc_208 \
		tgldmc_212 \
		tglguc_3520 \
		tglguc_6200 \
		tglhuc_750 \
		tglhuc_793
.endif

.if ${I915KMODS:Mrocketlake}
SUBDIR+=	rkldmc_202 \
		rkldmc_203
.endif

.if ${I915KMODS:Malderlake}
SUBDIR+=	adlpdmc \
		adlpdmc_210 \
		adlpdmc_212 \
		adlpguc_6203 \
		adlsdmc_201
.endif

.if ${I915KMODS:Mmeteorlake}
SUBDIR+=	mtldmc \
		mtldmc_210
.endif

.if ${I915KMODS:Mdg1}
SUBDIR+=	dg1dmc_202 \
		dg1guc_6200 \
		dg1huc \
		dg1huc_771 \
		dg1huc_793
.endif

.if ${I915KMODS:Mdg2}
SUBDIR+=	dg2dmc_206 \
		dg2dmc_207 \
		dg2dmc_208 \
		dg2guc_70 \
		dg2guc_7012 \
		dg2guc_7041 \
		dg2huc_gsc
.endif

SUBDIR_PARALLEL=

.include <bsd.subdir.mk>
