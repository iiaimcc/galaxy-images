FROM anupkumar/docker-ml-jupyterlab:galaxy-integration-0.2

ENV PIP_DISABLE_PIP_VERSION_CHECK=1 \
    PYTHONDONTWRITEBYTECODE=1

COPY requirements.txt /tmp/requirements.txt

RUN python3 -m pip install --no-cache-dir -r /tmp/requirements.txt \
    && python3 - <<'PY'
from packaging.version import Version
import jupyterlab

version = Version(jupyterlab.__version__)
assert version.major == 4, f"Expected JupyterLab 4.x, got {jupyterlab.__version__}"
print(f"Validated JupyterLab {jupyterlab.__version__}")
PY
