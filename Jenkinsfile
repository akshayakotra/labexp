pipeline {
  agent any
  stages {
stage ( ’ Clone Code ’) {
steps {
echo ’ Code cloned from GitHub ’
}
}
stage ( ’ Install Dependencies ’) {
steps {
sh ’ pip3 install -r requirements . txt ’
}
}
stage ( ’ Run Tests ’) {
steps {
sh ’ pytest test_app . py ’
}
}
stage ( ’ Deploy Application ’) {
steps {
sh ’’’
pkill -f " python3 app . py " || true
setsid python3 app . py > nohup . out 2 >&1 < / dev
,→ / null &
sleep 5
’’’
}
}
}
}
