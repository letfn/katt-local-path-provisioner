build: clean local-path-provisioner.yaml

local-path-provisioner.yaml:
	kustomize build clean > local-path-provisioner.yaml

diff: local-path-provisioner.yaml
	kustomize build . > diff.yaml
	diff local-path-provisioner.yaml diff.yaml
	rm -f diff.yaml

.PHONY: clean
clean:
	rm -f local-path-provisioner.yaml
