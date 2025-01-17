
Vagrant.configure("2") do |config|
    config.hostmanager.enabled = true 
    config.hostmanager.manage_host = true
        

    config.vm.define "MySqlDB" do |db|
        db.vm.box = "eurolinux-vagrant/centos-stream-9"
        db.vm.box_version = "9.0.43"
        db.vm.hostname = "MySqlDB"
        db.vm.network "private_network", ip: "192.168.56.50"
        db.vm.provider "virtualbox" do |vb|
            vb.memory = "600"
        end

    end
          

    config.vm.define "MemCache" do |mc|
        mc.vm.box = "eurolinux-vagrant/centos-stream-9"
        mc.vm.box_version = "9.0.43"
        mc.vm.hostname = "MemCache"
        mc.vm.network "private_network", ip: "192.168.56.51"
        mc.vm.provider "virtualbox" do |vb|
            vb.memory = "600"
        end
    end
        
    config.vm.define "RabbitMQ" do |rmq|
        rmq.vm.box = "eurolinux-vagrant/centos-stream-9"
        rmq.vm.box_version = "9.0.43"
        rmq.vm.hostname = "RabbitMQ"
        rmq.vm.network "private_network", ip: "192.168.56.52"
        rmq.vm.provider "virtualbox" do |vb|
            vb.memory = "1024"
        end
    end
        
    config.vm.define "java-app" do |app|
        app.vm.box = "eurolinux-vagrant/centos-stream-9"
        app.vm.box_version = "9.0.43"
        app.vm.hostname = "java-app"
        app.vm.network "private_network", ip: "192.168.56.53"
        app.vm.provider "virtualbox" do |vb|
            vb.memory = "800"
        end
    end
                  
    config.vm.define "web-app" do |web|
        web.vm.box = "ubuntu/jammy64"
        web.vm.hostname = "web-app"
        web.vm.network "private_network", ip: "192.168.56.54"
        web.vm.provider "virtualbox" do |vb|
            vb.gui = true
            vb.memory = "800"
        end
    end
                   
end

