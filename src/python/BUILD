python_requirement(requirements=["sagemaker==2.182.0"])

python_sources(name="lib")

pex_binary(
    name="pex",
    dependencies=[":lib"],
    entry_point="hello.py",
)
