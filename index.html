import React, { useState, useMemo } from 'react';
import { 
  Building2, 
  Users, 
  DollarSign, 
  MapPin, 
  Package, 
  TrendingUp, 
  Search, 
  Plus, 
  Filter,
  MoreVertical,
  Briefcase,
  ShieldAlert,
  ArrowUpRight,
  X,
  Edit2,
  Check
} from 'lucide-react';

// Mock data for initial state - Prices updated to realistic MYR values
const initialClients = [
  {
    id: '1',
    name: 'PetroGlobal Solutions',
    type: 'Enterprise',
    industry: 'Oil & Gas',
    region: 'North America',
    volume: 'High',
    status: 'Active Servicing',
    lastContact: '2026-08-25',
    dedicatedPrices: {
      coveralls: 195.00,
      jackets: 240.00,
      gloves: 55.00
    },
    totalRevenue: 5400000
  },
  {
    id: '2',
    name: 'BuildRight Construction',
    type: 'Mid-Market',
    industry: 'Construction',
    region: 'Europe',
    volume: 'Medium',
    status: 'In Negotiation',
    lastContact: '2026-08-27',
    dedicatedPrices: {
      coveralls: 225.00,
      jackets: 260.00,
      gloves: 65.00
    },
    totalRevenue: 1950000
  },
  {
    id: '3',
    name: 'AeroTech Manufacturing',
    type: 'Enterprise',
    industry: 'Manufacturing',
    region: 'Asia Pacific',
    volume: 'High',
    status: 'Prospect',
    lastContact: '2026-08-20',
    dedicatedPrices: {
      coveralls: 210.00,
      jackets: 250.00,
      gloves: 60.00
    },
    totalRevenue: 0
  },
  {
    id: '4',
    name: 'SafeChem Industries',
    type: 'Small Business',
    industry: 'Chemical',
    region: 'North America',
    volume: 'Low',
    status: 'Active Servicing',
    lastContact: '2026-08-28',
    dedicatedPrices: {
      coveralls: 260.00,
      jackets: 300.00,
      gloves: 78.00
    },
    totalRevenue: 370000
  }
];

const INDUSTRIES = ['Oil & Gas', 'Construction', 'Manufacturing', 'Chemical', 'Mining'];
const REGIONS = ['North America', 'Europe', 'Asia Pacific', 'Middle East', 'Latin America'];
const CLIENT_TYPES = ['Enterprise', 'Mid-Market', 'Small Business'];
const VOLUMES = ['High', 'Medium', 'Low'];
const STATUSES = ['Prospect', 'In Negotiation', 'Active Servicing', 'Churned'];

// Helper to format currency in MYR
const formatMYR = (value) => {
  return new Intl.NumberFormat('en-MY', { style: 'currency', currency: 'MYR', maximumFractionDigits: 0 }).format(value);
};

// Reusable component for the top statistics cards
const StatCard = ({ title, value, icon: Icon, trend, trendUp }) => (
  <div className="bg-white p-6 rounded-xl border border-gray-100 shadow-sm">
    <div className="flex justify-between items-start">
      <div>
        <p className="text-sm font-medium text-gray-500 mb-1">{title}</p>
        <h3 className="text-2xl font-bold text-gray-900">{value}</h3>
      </div>
      <div className="p-3 bg-blue-50 rounded-lg">
        <Icon className="w-6 h-6 text-blue-600" />
      </div>
    </div>
    {trend && (
      <div className="mt-4 flex items-center text-sm">
        <ArrowUpRight className={`w-4 h-4 mr-1 ${trendUp ? 'text-green-500' : 'text-red-500'}`} />
        <span className={trendUp ? 'text-green-600 font-medium' : 'text-red-600 font-medium'}>
          {trend}
        </span>
        <span className="text-gray-500 ml-2">vs last month</span>
      </div>
    )}
  </div>
);

export default function SafetyCRM() {
  // Main data state
  const [clients, setClients] = useState(initialClients);
  
  // UI Controls state
  const [searchTerm, setSearchTerm] = useState('');
  const [filterIndustry, setFilterIndustry] = useState('All');
  const [filterStatus, setFilterStatus] = useState('All');
  const [activeTab, setActiveTab] = useState('pipeline'); // 'pipeline', 'clients', 'all'
  
  // Modal State for New Client
  const [isModalOpen, setIsModalOpen] = useState(false);
  const [newClient, setNewClient] = useState({
    name: '',
    type: 'Mid-Market',
    industry: 'Oil & Gas',
    region: 'Asia Pacific',
    volume: 'Medium',
    status: 'Prospect',
    coverallsPrice: '',
    jacketsPrice: '',
    glovesPrice: ''
  });

  // Editing State for Inline Price Updates
  const [editingId, setEditingId] = useState(null);
  const [editPrices, setEditPrices] = useState({ coveralls: 0, jackets: 0, gloves: 0 });

  // Filter clients based on search, dropdowns, and active tab
  const filteredClients = useMemo(() => {
    return clients.filter(client => {
      const matchesSearch = client.name.toLowerCase().includes(searchTerm.toLowerCase());
      const matchesIndustry = filterIndustry === 'All' || client.industry === filterIndustry;
      const matchesStatus = filterStatus === 'All' || client.status === filterStatus;
      
      if (activeTab === 'pipeline') {
        return matchesSearch && matchesIndustry && ['Prospect', 'In Negotiation'].includes(client.status);
      }
      if (activeTab === 'clients') {
          return matchesSearch && matchesIndustry && ['Active Servicing'].includes(client.status);
      }
      return matchesSearch && matchesIndustry && matchesStatus;
    });
  }, [clients, searchTerm, filterIndustry, filterStatus, activeTab]);

  // Calculate dashboard statistics dynamically
  const stats = useMemo(() => {
    const totalRevenue = clients.reduce((acc, curr) => acc + curr.totalRevenue, 0);
    const activeClients = clients.filter(c => c.status === 'Active Servicing').length;
    const prospects = clients.filter(c => c.status === 'Prospect' || c.status === 'In Negotiation').length;
    
    return {
      revenue: formatMYR(totalRevenue),
      active: activeClients,
      pipeline: prospects
    };
  }, [clients]);

  // Handle adding a new client from the modal
  const handleAddClient = (e) => {
    e.preventDefault();
    const newClientData = {
      id: Math.random().toString(36).substr(2, 9), // Simple ID generation
      name: newClient.name,
      type: newClient.type,
      industry: newClient.industry,
      region: newClient.region,
      volume: newClient.volume,
      status: newClient.status,
      lastContact: new Date().toISOString().split('T')[0],
      dedicatedPrices: {
        coveralls: parseFloat(newClient.coverallsPrice) || 0,
        jackets: parseFloat(newClient.jacketsPrice) || 0,
        gloves: parseFloat(newClient.glovesPrice) || 0
      },
      totalRevenue: 0 // Starts at 0 for new prospects
    };
    
    setClients([...clients, newClientData]);
    setIsModalOpen(false);
    
    // Reset form to defaults
    setNewClient({
      name: '', type: 'Mid-Market', industry: 'Oil & Gas', region: 'Asia Pacific',
      volume: 'Medium', status: 'Prospect', coverallsPrice: '', jacketsPrice: '', glovesPrice: ''
    });
  };

  // Setup inline editing mode for a row
  const startEditing = (client) => {
    setEditingId(client.id);
    setEditPrices({
      coveralls: client.dedicatedPrices.coveralls,
      jackets: client.dedicatedPrices.jackets,
      gloves: client.dedicatedPrices.gloves
    });
  };

  // Save the updated prices to the client data
  const savePrices = (id) => {
    setClients(clients.map(c => {
      if (c.id === id) {
        return {
          ...c,
          dedicatedPrices: {
            coveralls: parseFloat(editPrices.coveralls) || 0,
            jackets: parseFloat(editPrices.jackets) || 0,
            gloves: parseFloat(editPrices.gloves) || 0
          }
        };
      }
      return c;
    }));
    setEditingId(null);
  };

  // Helper to color-code statuses
  const getStatusColor = (status) => {
    switch(status) {
      case 'Active Servicing': return 'bg-emerald-100 text-emerald-700';
      case 'In Negotiation': return 'bg-amber-100 text-amber-700';
      case 'Prospect': return 'bg-blue-100 text-blue-700';
      default: return 'bg-gray-100 text-gray-700';
    }
  };

  return (
    <div className="min-h-screen bg-gray-50 font-sans text-gray-900 relative">
      {/* Top Navigation */}
      <header className="bg-white border-b border-gray-200 sticky top-0 z-10">
        <div className="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 h-16 flex items-center justify-between">
          <div className="flex items-center gap-3">
            <div className="bg-blue-600 p-2 rounded-lg">
              <ShieldAlert className="w-6 h-6 text-white" />
            </div>
            <div>
              <h1 className="text-xl font-bold leading-tight">SafeGuard CRM</h1>
              <p className="text-xs text-gray-500 font-medium">Safety Equipment Division (MYR)</p>
            </div>
          </div>
          <div className="flex items-center gap-4">
            <button className="p-2 text-gray-400 hover:text-gray-600 transition-colors">
              <Search className="w-5 h-5" />
            </button>
            <div className="w-8 h-8 rounded-full bg-gradient-to-tr from-blue-600 to-indigo-600 text-white flex items-center justify-center font-bold text-sm shadow-sm">
              CS
            </div>
          </div>
        </div>
      </header>

      <main className="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-8">
        
        {/* Dashboard Stats */}
        <div className="grid grid-cols-1 md:grid-cols-3 gap-6 mb-8">
          <StatCard 
            title="Total Revenue (YTD)" 
            value={stats.revenue} 
            icon={DollarSign}
            trend="12.5%"
            trendUp={true}
          />
          <StatCard 
            title="Active Service Accounts" 
            value={stats.active} 
            icon={Briefcase}
            trend="4.2%"
            trendUp={true}
          />
          <StatCard 
            title="Acquisition Pipeline" 
            value={stats.pipeline} 
            icon={TrendingUp}
            trend="2.1%"
            trendUp={false}
          />
        </div>

        <div className="bg-white rounded-xl shadow-sm border border-gray-100 p-5 mb-6 flex flex-col sm:flex-row justify-between items-center gap-4">
          
          <div className="flex space-x-1 bg-gray-100 p-1 rounded-lg self-start sm:self-auto w-full sm:w-auto overflow-x-auto">
            <button 
              onClick={() => setActiveTab('pipeline')}
              className={`px-4 py-2 text-sm font-medium rounded-md transition-all whitespace-nowrap ${activeTab === 'pipeline' ? 'bg-white text-blue-600 shadow-sm' : 'text-gray-600 hover:text-gray-900'}`}
            >
              Acquisition
            </button>
            <button 
              onClick={() => setActiveTab('clients')}
              className={`px-4 py-2 text-sm font-medium rounded-md transition-all whitespace-nowrap ${activeTab === 'clients' ? 'bg-white text-blue-600 shadow-sm' : 'text-gray-600 hover:text-gray-900'}`}
            >
              Client Servicing
            </button>
            <button 
              onClick={() => setActiveTab('all')}
              className={`px-4 py-2 text-sm font-medium rounded-md transition-all whitespace-nowrap ${activeTab === 'all' ? 'bg-white text-blue-600 shadow-sm' : 'text-gray-600 hover:text-gray-900'}`}
            >
              All Data
            </button>
          </div>

          <div className="flex flex-col sm:flex-row items-center gap-3 w-full sm:w-auto">
            <div className="relative w-full sm:w-64">
              <Search className="absolute left-3 top-1/2 transform -translate-y-1/2 text-gray-400 w-4 h-4" />
              <input 
                type="text" 
                placeholder="Search clients..." 
                className="w-full pl-9 pr-4 py-2 text-sm border border-gray-200 rounded-lg focus:outline-none focus:ring-2 focus:ring-blue-500 focus:border-transparent transition-all"
                value={searchTerm}
                onChange={(e) => setSearchTerm(e.target.value)}
              />
            </div>
            
            <div className="relative w-full sm:w-auto">
              <select 
                className="w-full appearance-none pl-10 pr-8 py-2 text-sm border border-gray-200 rounded-lg focus:outline-none focus:ring-2 focus:ring-blue-500 bg-white"
                value={filterIndustry}
                onChange={(e) => setFilterIndustry(e.target.value)}
              >
                <option value="All">All Industries</option>
                {INDUSTRIES.map(ind => <option key={ind} value={ind}>{ind}</option>)}
              </select>
              <Filter className="absolute left-3 top-1/2 transform -translate-y-1/2 text-gray-400 w-4 h-4" />
            </div>

            <button 
              onClick={() => setIsModalOpen(true)}
              className="w-full sm:w-auto bg-blue-600 hover:bg-blue-700 text-white px-4 py-2 rounded-lg text-sm font-medium flex items-center justify-center transition-colors whitespace-nowrap"
            >
              <Plus className="w-4 h-4 mr-2" />
              New Client
            </button>
          </div>
        </div>

        <div className="bg-white rounded-xl shadow-sm border border-gray-100 overflow-hidden w-full">
          <div className="overflow-x-auto">
            <table className="w-full text-left border-collapse min-w-[800px]">
              <thead>
                <tr className="bg-gray-50 border-b border-gray-200">
                  <th className="px-6 py-4 text-xs font-semibold text-gray-500 uppercase tracking-wider">Client Info</th>
                  <th className="px-6 py-4 text-xs font-semibold text-gray-500 uppercase tracking-wider">Status & Phase</th>
                  <th className="px-6 py-4 text-xs font-semibold text-gray-500 uppercase tracking-wider">Dedicated Pricing (MYR)</th>
                  <th className="px-6 py-4 text-xs font-semibold text-gray-500 uppercase tracking-wider">Volume & Revenue</th>
                  <th className="px-6 py-4 text-xs font-semibold text-gray-500 uppercase tracking-wider text-right">Actions</th>
                </tr>
              </thead>
              <tbody className="divide-y divide-gray-100">
                {filteredClients.length > 0 ? (
                  filteredClients.map((client) => (
                    <tr key={client.id} className="hover:bg-gray-50/50 transition-colors">
                      <td className="px-6 py-4">
                        <div className="flex items-center">
                          <div className="w-10 h-10 rounded-lg bg-gray-100 flex items-center justify-center text-gray-500 font-bold border border-gray-200 flex-shrink-0">
                            {client.name.charAt(0)}
                          </div>
                          <div className="ml-4">
                            <div className="font-semibold text-gray-900">{client.name}</div>
                            <div className="text-xs text-gray-500 flex items-center mt-1">
                              <Building2 className="w-3 h-3 mr-1" /> {client.industry}
                              <span className="mx-2 text-gray-300">•</span>
                              <MapPin className="w-3 h-3 mr-1" /> {client.region}
                            </div>
                          </div>
                        </div>
                      </td>
                      
                      <td className="px-6 py-4">
                        <span className={`inline-flex items-center px-2.5 py-1 rounded-full text-xs font-medium ${getStatusColor(client.status)}`}>
                          {client.status}
                        </span>
                        <div className="text-xs text-gray-500 mt-2">
                          Type: <span className="font-medium text-gray-700">{client.type}</span>
                        </div>
                      </td>
                      
                      <td className="px-6 py-4 w-64">
                        <div className="text-sm relative group">
                          {editingId === client.id ? (
                            <div className="space-y-2 bg-gray-50 p-2 rounded-lg border border-gray-200">
                              <div className="flex items-center gap-2">
                                <span className="text-gray-500 w-16 text-xs">Cvralls:</span>
                                <input type="number" className="w-full p-1 border rounded text-xs" value={editPrices.coveralls} onChange={(e) => setEditPrices({...editPrices, coveralls: e.target.value})} />
                              </div>
                              <div className="flex items-center gap-2">
                                <span className="text-gray-500 w-16 text-xs">Jckts:</span>
                                <input type="number" className="w-full p-1 border rounded text-xs" value={editPrices.jackets} onChange={(e) => setEditPrices({...editPrices, jackets: e.target.value})} />
                              </div>
                              <div className="flex items-center gap-2">
                                <span className="text-gray-500 w-16 text-xs">Glvs:</span>
                                <input type="number" className="w-full p-1 border rounded text-xs" value={editPrices.gloves} onChange={(e) => setEditPrices({...editPrices, gloves: e.target.value})} />
                              </div>
                              <button onClick={() => savePrices(client.id)} className="w-full mt-1 flex items-center justify-center text-xs text-white bg-green-600 hover:bg-green-700 px-2 py-1.5 rounded transition-colors">
                                <Check className="w-3 h-3 mr-1" /> Save Prices
                              </button>
                            </div>
                          ) : (
                            <div className="pr-6">
                              <div className="flex justify-between items-center mb-1">
                                <span className="text-gray-500">Coveralls:</span>
                                <span className="font-medium">RM {client.dedicatedPrices.coveralls.toFixed(2)}</span>
                              </div>
                              <div className="flex justify-between items-center mb-1">
                                <span className="text-gray-500">Jackets:</span>
                                <span className="font-medium">RM {client.dedicatedPrices.jackets.toFixed(2)}</span>
                              </div>
                              <div className="flex justify-between items-center">
                                <span className="text-gray-500">Gloves:</span>
                                <span className="font-medium">RM {client.dedicatedPrices.gloves.toFixed(2)}</span>
                              </div>
                              <button 
                                onClick={() => startEditing(client)}
                                className="absolute right-0 top-0 p-1.5 bg-white border border-gray-200 shadow-sm rounded-md text-gray-500 hover:text-blue-600 opacity-0 group-hover:opacity-100 transition-opacity"
                                title="Edit Pricing"
                              >
                                <Edit2 className="w-4 h-4" />
                              </button>
                            </div>
                          )}
                        </div>
                      </td>
                      
                      <td className="px-6 py-4">
                        <div className="flex items-center mb-2">
                          <Package className="w-4 h-4 text-gray-400 mr-2" />
                          <span className={`text-sm font-medium ${
                            client.volume === 'High' ? 'text-green-600' : 
                            client.volume === 'Medium' ? 'text-amber-600' : 'text-gray-600'
                          }`}>
                            {client.volume} Vol.
                          </span>
                        </div>
                        <div className="text-sm font-semibold text-gray-900">
                          {client.totalRevenue > 0 ? `RM ${(client.totalRevenue / 1000).toFixed(1)}k` : 'RM 0'}
                        </div>
                      </td>
                      
                      <td className="px-6 py-4 text-right">
                        <button className="text-gray-400 hover:text-gray-600 p-1 rounded-md hover:bg-gray-100 transition-colors">
                          <MoreVertical className="w-5 h-5" />
                        </button>
                      </td>
                    </tr>
                  ))
                ) : (
                  <tr>
                    <td colSpan="5" className="px-6 py-12 text-center text-gray-500">
                      <div className="flex flex-col items-center">
                        <ShieldAlert className="w-12 h-12 text-gray-300 mb-3" />
                        <p className="text-base font-medium text-gray-900">No clients found</p>
                        <p className="text-sm mt-1">Try adjusting your filters or search term.</p>
                      </div>
                    </td>
                  </tr>
                )}
              </tbody>
            </table>
          </div>
          
          <div className="bg-gray-50 px-6 py-4 border-t border-gray-200 flex flex-col sm:flex-row items-center justify-between gap-4">
            <p className="text-sm text-gray-500">
              Showing <span className="font-medium">{filteredClients.length}</span> of <span className="font-medium">{clients.length}</span> entries
            </p>
            <div className="flex gap-2">
              <button className="px-3 py-1 text-sm border border-gray-200 rounded-md bg-white text-gray-600 hover:bg-gray-50 disabled:opacity-50">Previous</button>
              <button className="px-3 py-1 text-sm border border-gray-200 rounded-md bg-white text-gray-600 hover:bg-gray-50 disabled:opacity-50">Next</button>
            </div>
          </div>
        </div>
      </main>

      {isModalOpen && (
        <div className="fixed inset-0 bg-black/50 flex items-center justify-center z-50 p-4">
          <div className="bg-white rounded-xl shadow-xl w-full max-w-2xl overflow-hidden max-h-[90vh] flex flex-col">
            <div className="px-6 py-4 border-b border-gray-200 flex justify-between items-center bg-gray-50">
              <h2 className="text-lg font-semibold text-gray-900">Add New Client</h2>
              <button onClick={() => setIsModalOpen(false)} className="text-gray-400 hover:text-gray-600 bg-white rounded-md p-1 border border-gray-200">
                <X className="w-5 h-5" />
              </button>
            </div>
            
            <form onSubmit={handleAddClient} className="p-6 overflow-y-auto">
              <div className="grid grid-cols-1 md:grid-cols-2 gap-8 mb-6">
                {/* Basic Info */}
                <div className="space-y-4">
                  <h3 className="text-sm font-semibold text-blue-600 uppercase tracking-wider border-b pb-2">Client Details</h3>
                  <div>
                    <label className="block text-sm font-medium text-gray-700 mb-1">Company Name *</label>
                    <input required type="text" className="w-full p-2.5 border border-gray-300 rounded-lg text-sm focus:ring-2 focus:ring-blue-500 focus:border-blue-500 outline-none transition-all" value={newClient.name} onChange={e => setNewClient({...newClient, name: e.target.value})} />
                  </div>
                  <div>
                    <label className="block text-sm font-medium text-gray-700 mb-1">Industry</label>
                    <select className="w-full p-2.5 border border-gray-300 rounded-lg text-sm focus:ring-2 focus:ring-blue-500 outline-none transition-all bg-white" value={newClient.industry} onChange={e => setNewClient({...newClient, industry: e.target.value})}>
                      {INDUSTRIES.map(i => <option key={i} value={i}>{i}</option>)}
                    </select>
                  </div>
                  <div>
                    <label className="block text-sm font-medium text-gray-700 mb-1">Region</label>
                    <select className="w-full p-2.5 border border-gray-300 rounded-lg text-sm focus:ring-2 focus:ring-blue-500 outline-none transition-all bg-white" value={newClient.region} onChange={e => setNewClient({...newClient, region: e.target.value})}>
                      {REGIONS.map(r => <option key={r} value={r}>{r}</option>)}
                    </select>
                  </div>
                  <div>
                    <label className="block text-sm font-medium text-gray-700 mb-1">Client Size/Type</label>
                    <select className="w-full p-2.5 border border-gray-300 rounded-lg text-sm focus:ring-2 focus:ring-blue-500 outline-none transition-all bg-white" value={newClient.type} onChange={e => setNewClient({...newClient, type: e.target.value})}>
                      {CLIENT_TYPES.map(t => <option key={t} value={t}>{t}</option>)}
                    </select>
                  </div>
                </div>

                {/* Status & Pricing */}
                <div className="space-y-4">
                  <h3 className="text-sm font-semibold text-blue-600 uppercase tracking-wider border-b pb-2">Status & Pricing (MYR)</h3>
                  <div>
                    <label className="block text-sm font-medium text-gray-700 mb-1">Pipeline Status</label>
                    <select className="w-full p-2.5 border border-gray-300 rounded-lg text-sm focus:ring-2 focus:ring-blue-500 outline-none transition-all bg-white" value={newClient.status} onChange={e => setNewClient({...newClient, status: e.target.value})}>
                      {STATUSES.map(s => <option key={s} value={s}>{s}</option>)}
                    </select>
                  </div>
                  <div>
                    <label className="block text-sm font-medium text-gray-700 mb-1">Volume Expectation</label>
                    <select className="w-full p-2.5 border border-gray-300 rounded-lg text-sm focus:ring-2 focus:ring-blue-500 outline-none transition-all bg-white" value={newClient.volume} onChange={e => setNewClient({...newClient, volume: e.target.value})}>
                      {VOLUMES.map(v => <option key={v} value={v}>{v}</option>)}
                    </select>
                  </div>
                  
                  <div className="pt-2 bg-gray-50 p-4 rounded-lg border border-gray-100">
                    <label className="block text-sm font-medium text-gray-900 mb-3">Dedicated Pricing Limits</label>
                    <div className="space-y-3">
                      <div className="flex items-center gap-3">
                        <span className="text-sm font-medium text-gray-500 w-20">Coveralls</span>
                        <div className="relative flex-1">
                          <span className="absolute left-3 top-1/2 -translate-y-1/2 text-gray-500 text-sm">RM</span>
                          <input type="number" placeholder="0.00" className="w-full pl-9 p-2 border border-gray-300 rounded-md text-sm focus:ring-2 focus:ring-blue-500 outline-none" value={newClient.coverallsPrice} onChange={e => setNewClient({...newClient, coverallsPrice: e.target.value})} />
                        </div>
                      </div>
                      <div className="flex items-center gap-3">
                        <span className="text-sm font-medium text-gray-500 w-20">Jackets</span>
                        <div className="relative flex-1">
                          <span className="absolute left-3 top-1/2 -translate-y-1/2 text-gray-500 text-sm">RM</span>
                          <input type="number" placeholder="0.00" className="w-full pl-9 p-2 border border-gray-300 rounded-md text-sm focus:ring-2 focus:ring-blue-500 outline-none" value={newClient.jacketsPrice} onChange={e => setNewClient({...newClient, jacketsPrice: e.target.value})} />
                        </div>
                      </div>
                      <div className="flex items-center gap-3">
                        <span className="text-sm font-medium text-gray-500 w-20">Gloves</span>
                        <div className="relative flex-1">
                          <span className="absolute left-3 top-1/2 -translate-y-1/2 text-gray-500 text-sm">RM</span>
                          <input type="number" placeholder="0.00" className="w-full pl-9 p-2 border border-gray-300 rounded-md text-sm focus:ring-2 focus:ring-blue-500 outline-none" value={newClient.glovesPrice} onChange={e => setNewClient({...newClient, glovesPrice: e.target.value})} />
                        </div>
                      </div>
                    </div>
                  </div>
                </div>
              </div>
              
              <div className="flex justify-end gap-3 pt-4 border-t border-gray-200">
                <button type="button" onClick={() => setIsModalOpen(false)} className="px-5 py-2.5 text-sm font-medium text-gray-700 bg-white border border-gray-300 rounded-lg hover:bg-gray-50 transition-colors">
                  Cancel
                </button>
                <button type="submit" className="px-5 py-2.5 text-sm font-medium text-white bg-blue-600 rounded-lg hover:bg-blue-700 shadow-sm transition-colors flex items-center">
                  <Check className="w-4 h-4 mr-2" />
                  Save Client
                </button>
              </div>
            </form>
          </div>
        </div>
      )}

    </div>
  );
}
