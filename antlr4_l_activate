#!/usr/bin/env bash
# Activate antlr4-l environment
printf "%s\n" "Activating antlr4.sh in restricted mode."

antlr4_l_stop() {
  # Unset -_ANTLR4_L_VENV variable.
  if [[ ! -z "${_ANTLR4_L_VENV+_}" ]]; then
    unset _ANTLR4_L_VENV
  fi

  # Reset path
  if [[ ! -z "${_OLD_PATH+_}" ]]; then
    PATH="${_OLD_PATH}"
    export PATH
    unset _OLD_PATH
  fi

  # Forget passed command.
  if [[ -n "${BASH-}" ]] && [[ -n "${ZSH_VERSION-}" ]]; then
    hash -r 2>/dev/null
  fi

  if [[ "${1:-}" != "safe" ]]; then
    unset -f antlr4_l_stop
  fi
}

antlr4_l_stop safe

# Export _ANTLR4_L_VENV.
_ANTLR4_L_VENV="/home/jeffryangtoni/sources/github/learning/antlr-learning"
export _ANTLR4_L_VENV

# Export new path
_OLD_PATH="${PATH}"
PATH="${_ANTLR4_L_VENV}:${PATH}"
export PATH

if [[ -n "${BASH-}" ]] && [[ -n "${ZSH_VERSION-}" ]]; then
  hash -r 2>/dev/null
fi

printf "%s\n" "You can use 'antlr4_l' now inside current directory."
