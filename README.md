# Shellscripts

SERVICE="$(ps -o args= $PPID | awk "{print \$NF}")"
if [[ ${SERVICE} == 'start' ||  ${SERVICE} == 'restart' ]]; then
    update_config
fi
