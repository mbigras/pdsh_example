vms = [
    { 'name' => 'foo.example.com', 'ip' => '192.168.52.10' },
    { 'name' => 'bar.example.com', 'ip' => '192.168.52.11' },
    { 'name' => 'baz.example.com', 'ip' => '192.168.52.12' },
]

Vagrant.configure('2') do |config|
    config.ssh.insert_key = false
    vms.each do |host|
        config.vm.define host['name'] do |t|
            t.vm.box = 'generic/ubuntu1604'
            t.vm.hostname = host['name']
            t.vm.network(:private_network, ip: host['ip'])
            t.vm.provider 'virtualbox' do |v|
              v.memory = host['memory'] || 2048
            end
        end
    end
end
