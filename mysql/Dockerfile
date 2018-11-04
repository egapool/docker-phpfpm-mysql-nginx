FROM mysql:5.7

COPY initial.sql /docker-entrypoint-initdb.d/initial.sql

# modify my.cnf
#RUN sed -i -e "s/^sql_mode=.*$/sql_mode=NO_ENGINE_SUBSTITUTION/" /etc/mysql/my.cnf
RUN echo "[mysqld]" >> /etc/mysql/my.cnf
RUN echo sql_mode=NO_ENGINE_SUBSTITUTION >> /etc/mysql/my.cnf
