cmake_minimum_required (VERSION 2.8.10)
project (pbtemplate)

include (pixelboost/build.cmake)

pixelboost_setup_pre(pixelboost pbtemplate "com.pixelboost.template" "Pixelboost Template")

include_directories("source")

set (CORE_SOURCES
	"source/core/game.cpp"
	"source/core/game.h"
	)

set (SCREEN_SOURCES
	"source/screens/gameScreen.cpp"
	"source/screens/gameScreen.h"
	"source/screens/menuScreen.cpp"
	"source/screens/menuScreen.h"
	)

set (TEMPLATE_SOURCES
	${CORE_SOURCES}
	${SCREEN_SOURCES}
	)

source_group (core FILES ${CORE_SOURCES})
source_group (screens FILES ${SCREEN_SOURCES})

pixelboost_setup_post("${TEMPLATE_SOURCES}")
