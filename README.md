# kube.plex

echo "# kube.plex" >> README.md
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin git@github.com:thlasta/kube.plex.git
git push -u origin main

# Namespace**
# We are going to isolate all the Kubernetes objects related to Pi-Hole in the namespace pihole.
# To create a namespace, run the following command:
$ kubectl create namespace plexserver

# Repo clonen
git clone git@github.com:thlasta/kube.plex.git

# Repo auschecken/holen
git pull git@github.com:thlasta/kube.plex.git

# Bei Änderungen:
git commit -m "Änderungsbeschreibung"
git push --all

# Jump one folder up, and apply to the whole folder:
kubectl apply -f plexserver/


