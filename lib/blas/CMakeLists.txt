#blas library

SET (BLAS_LIB_SRCS
	${CMAKE_CURRENT_SOURCE_DIR}/blas.h
	${CMAKE_CURRENT_SOURCE_DIR}/blasp.h
	${CMAKE_CURRENT_SOURCE_DIR}/daxpy.c
	${CMAKE_CURRENT_SOURCE_DIR}/ddot.c
	${CMAKE_CURRENT_SOURCE_DIR}/dnrm2.c
	${CMAKE_CURRENT_SOURCE_DIR}/dscal.c
	)

ADD_LIBRARY(${BLAS_LIBRARIES} ${LINKING_MODE}
	${BLAS_LIB_SRCS}
)

INSTALL(TARGETS ${BLAS_LIBRARIES} RUNTIME DESTINATION bin LIBRARY DESTINATION bin ARCHIVE DESTINATION bin)

