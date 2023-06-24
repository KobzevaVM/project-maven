# Сборка project-maven

1. Скачать проект из репозитория https://github.com/KobzevaVM/project-maven
2. Выполни команду, которая написана ниже в терминале из директории с проектом.
	 
	 Это необходимо для корректной сборки зависимости com.javarush: desktop-game-engine:1.0, в pom.xml подробная инструкция о зависимости.

	mvn \
	deploy:deploy-file \
	-Durl=file:./lib \
	-Dfile=./lib/desktop-game-engine.jar \
	-DgroupId=com.javarush \
	-DartifactId=desktop-game-engine \
	-Dpackaging=jar \
	-Dversion=1.0

4. Из директории проекта в терминале прописать "mvn clear install"
5. Итоговый jar файл сохраниться в локальный репозиторий maven ~/.m2/repository/
6. Из любой директории можно вызвать запуск jar файла командой в терминале:

	java -jar ~/.m2/repository/jru/module3/project-maven/1.0/project-maven-1.0.jar
