 OrangeOne Maven Repository
========================

Maven pom.xml
--------------------

	<repositories>
		<repository>
			<id>third</id>
			<url>https://orangeone.github.io/repos/third/</url>
		</repository>
	</repositories>


Ivy ivysettings.xml
--------------------

	<ivysettings>
		<settings defaultResolver="default" />
		<resolvers>
			<chain name="public">
				<ibiblio name="maven" m2compatible="true" />
				<ibiblio name="third" m2compatible="true" root="https://orangeone.github.io/repos/third/" />
			</chain>
		</resolvers>
		<include url="${ivy.default.settings.dir}/ivysettings-shared.xml" />
		<include url="${ivy.default.settings.dir}/ivysettings-local.xml" />
		<include url="${ivy.default.settings.dir}/ivysettings-main-chain.xml" />
		<include url="${ivy.default.settings.dir}/ivysettings-default-chain.xml" />
	</ivysettings>
