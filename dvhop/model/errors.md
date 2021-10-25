../src/dvhop/model/distance-table.cc: In member function ‘void ns3::dvhop::DistanceTable::AddBeacon(ns3::Ipv4Address, uint16_t, double, double)’:
../src/dvhop/model/distance-table.cc:55:59: error: cannot bind rvalue reference of type ‘double&&’ to lvalue of type ‘double’
   55 |           info.SetPosition (std::make_pair<double,double>(xPos, yPos));
      |                                                           ^~~~
In file included from /usr/include/c++/9/bits/stl_algobase.h:64,
                 from /usr/include/c++/9/bits/stl_tree.h:63,
                 from /usr/include/c++/9/map:60,
                 from ../src/dvhop/model/distance-table.h:4,
                 from ../src/dvhop/model/distance-table.cc:1:
/usr/include/c++/9/bits/stl_pair.h:524:21: note:   initializing argument 1 of ‘constexpr std::pair<typename std::__decay_and_strip<_Tp>::__type, typename std::__decay_and_strip<_T2>::__type> std::make_pair(_T1&&, _T2&&) [with _T1 = double; _T2 = double; typename std::__decay_and_strip<_T2>::__type = double; typename std::__decay_and_strip<_Tp>::__type = double]’
  524 |     make_pair(_T1&& __x, _T2&& __y)
      |               ~~~~~~^~~
../src/dvhop/model/distance-table.cc:57:67: error: cannot bind rvalue reference of type ‘ns3::Ipv4Address&&’ to lvalue of type ‘ns3::Ipv4Address’
   57 |           m_table.insert (std::make_pair<Ipv4Address, BeaconInfo>(beacon, info));
      |                                                                   ^~~~~~
In file included from /usr/include/c++/9/bits/stl_algobase.h:64,
                 from /usr/include/c++/9/bits/stl_tree.h:63,
                 from /usr/include/c++/9/map:60,
                 from ../src/dvhop/model/distance-table.h:4,
                 from ../src/dvhop/model/distance-table.cc:1:
/usr/include/c++/9/bits/stl_pair.h:524:21: note:   initializing argument 1 of ‘constexpr std::pair<typename std::__decay_and_strip<_Tp>::__type, typename std::__decay_and_strip<_T2>::__type> std::make_pair(_T1&&, _T2&&) [with _T1 = ns3::Ipv4Address; _T2 = ns3::dvhop::BeaconInfo; typename std::__decay_and_strip<_T2>::__type = ns3::dvhop::BeaconInfo; typename std::__decay_and_strip<_Tp>::__type = ns3::Ipv4Address]’
  524 |     make_pair(_T1&& __x, _T2&& __y)
      |               ~~~~~~^~~

In file included from ./ns3/object-base.h:23,
                 from ./ns3/object.h:29,
                 from ./ns3/node.h:26,
                 from ../src/dvhop/model/dvhop.h:5,
                 from ../src/dvhop/model/dvhop.cc:3:
./ns3/type-id.h: In instantiation of ‘static ns3::ObjectBase* ns3::TypeId::AddConstructor()::Maker::Create() [with T = ns3::dvhop::RoutingProtocol]’:
./ns3/type-id.h:659:3:   required from ‘ns3::TypeId ns3::TypeId::AddConstructor() [with T = ns3::dvhop::RoutingProtocol]’
../src/dvhop/model/dvhop.cc:32:45:   required from here
./ns3/type-id.h:656:27: error: invalid new-expression of abstract class type ‘ns3::dvhop::RoutingProtocol’
  656 |       ObjectBase * base = new T ();
      |                           ^~~~~~~~
In file included from ../src/dvhop/model/dvhop.cc:3:
../src/dvhop/model/dvhop.h:24:11: note:   because the following virtual functions are pure within ‘ns3::dvhop::RoutingProtocol’:
   24 |     class RoutingProtocol : public Ipv4RoutingProtocol{
      |           ^~~~~~~~~~~~~~~
In file included from ../src/dvhop/model/dvhop.h:8,
                 from ../src/dvhop/model/dvhop.cc:3:
./ns3/ipv4-routing-protocol.h:172:16: note: 	‘virtual void ns3::Ipv4RoutingProtocol::PrintRoutingTable(ns3::Ptr<ns3::OutputStreamWrapper>, ns3::Time::Unit) const’
  172 |   virtual void PrintRoutingTable (Ptr<OutputStreamWrapper> stream, Time::Unit unit = Time::S) const = 0;
      |                ^~~~~~~~~~~~~~~~~

