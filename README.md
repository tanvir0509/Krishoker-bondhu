# // File: App.js import React from 'react'; import { NavigationContainer } from '@react-navigation/native'; import { createNativeStackNavigator } from '@react-navigation/native-stack'; import HomeScreen from './src/screens/HomeScreen'; import WeatherScreen from './src/screens/WeatherScreen'; import CropAdviceScreen from './src/screens/CropAdviceScreen'; import MarketPriceScreen from './src/screens/MarketPriceScreen'; import TrainingScreen from './src/screens/TrainingScreen'; import CalendarScreen from './src/screens/CalendarScreen'; import CommunityScreen from './src/screens/CommunityScreen'; import GovernmentSupportScreen from './src/screens/GovernmentSupportScreen'; import OfflineContentScreen from './src/screens/OfflineContentScreen'; import ImageHelpScreen from './src/screens/ImageHelpScreen';

const Stack = createNativeStackNavigator();

export default function App() { return ( <NavigationContainer> <Stack.Navigator initialRouteName="Home"> <Stack.Screen name="Home" component={HomeScreen} /> <Stack.Screen name="Weather" component={WeatherScreen} /> <Stack.Screen name="CropAdvice" component={CropAdviceScreen} /> <Stack.Screen name="MarketPrice" component={MarketPriceScreen} /> <Stack.Screen name="Training" component={TrainingScreen} /> <Stack.Screen name="Calendar" component={CalendarScreen} /> <Stack.Screen name="Community" component={CommunityScreen} /> <Stack.Screen name="GovernmentSupport" component={GovernmentSupportScreen} /> <Stack.Screen name="OfflineContent" component={OfflineContentScreen} /> <Stack.Screen name="ImageHelp" component={ImageHelpScreen} /> </Stack.Navigator> </NavigationContainer> ); }

// File: src/screens/HomeScreen.js import React from 'react'; import { View, Text, Button, ScrollView } from 'react-native';

export default function HomeScreen({ navigation }) { return ( <ScrollView contentContainerStyle={{ padding: 20 }}> <Text style={{ fontSize: 24, fontWeight: 'bold', marginBottom: 20 }}>🌾 কৃষি বন্ধু অ্যাপে স্বাগতম</Text> <Button title="আবহাওয়া" onPress={() => navigation.navigate('Weather')} /> <Button title="ফসল পরামর্শ" onPress={() => navigation.navigate('CropAdvice')} /> <Button title="বাজার মূল্য" onPress={() => navigation.navigate('MarketPrice')} /> <Button title="সরকারি সহায়তা" onPress={() => navigation.navigate('GovernmentSupport')} /> <Button title="প্রশিক্ষণ" onPress={() => navigation.navigate('Training')} /> <Button title="কৃষি ক্যালেন্ডার" onPress={() => navigation.navigate('Calendar')} /> <Button title="কমিউনিটি ফোরাম" onPress={() => navigation.navigate('Community')} /> <Button title="ছবি তুলে সহায়তা" onPress={() => navigation.navigate('ImageHelp')} /> <Button title="অফলাইন তথ্য" onPress={() => navigation.navigate('OfflineContent')} /> </ScrollView> ); }

// File: src/screens/WeatherScreen.js import React from 'react'; import { View, Text } from 'react-native';

export default function WeatherScreen() { return ( <View style={{ padding: 20 }}> <Text style={{ fontSize: 20 }}>আজকের আবহাওয়া:</Text> <Text>🌧️ বৃষ্টি সম্ভাবনা: ৬০%</Text> <Text>🌡️ তাপমাত্রা: ৩২°C</Text> <Text>💧 আর্দ্রতা: ৭০%</Text> <Text>🗓️ ঋতুভিত্তিক পূর্বাভাস: বর্ষা</Text> </View> ); }

// File: src/screens/CropAdviceScreen.js import React from 'react'; import { View, Text } from 'react-native';

export default function CropAdviceScreen() { return ( <View style={{ padding: 20 }}> <Text style={{ fontSize: 20 }}>ফসল পরামর্শ:</Text> <Text>🌾 এই মৌসুমে ধান ভালো হবে</Text> <Text>🌱 উন্নত বীজ: BRRI-28, BRRI-50</Text> <Text>🐛 কীটনাশক: নির্দিষ্ট মাত্রায় ব্যবহার করুন</Text> <Text>👨‍🌾 চাষ পদ্ধতি: জৈব পদ্ধতির চেষ্টা করুন</Text> </View> ); }

// File: src/screens/MarketPriceScreen.js import React from 'react'; import { View, Text } from 'react-native';

export default function MarketPriceScreen() { return ( <View style={{ padding: 20 }}> <Text style={{ fontSize: 20 }}>বাজার দর:</Text> <Text>ধান: ১২০০ টাকা / মণ</Text> <Text>পেঁয়াজ: ৪০ টাকা / কেজি</Text> <Text>লালশাক: ১৫ টাকা / আঁটি</Text> </View> ); }

// File: src/screens/TrainingScreen.js import React from 'react'; import { View, Text, Linking, Button } from 'react-native';

export default function TrainingScreen() { return ( <View style={{ padding: 20 }}> <Text style={{ fontSize: 20 }}>প্রশিক্ষণ ভিডিও:</Text> <Button title="জৈব চাষ পদ্ধতি" onPress={() => Linking.openURL('https://www.youtube.com/watch?v=1vxw6Kzpy9E')} /> <Button title="ফলমূল চাষ" onPress={() => Linking.openURL('https://www.youtube.com/watch?v=ABCD1234')} /> </View> ); }

// File: src/screens/CalendarScreen.js import React from 'react'; import { View, Text } from 'react-native';

export default function CalendarScreen() { return ( <View style={{ padding: 20 }}> <Text style={{ fontSize: 20 }}>কৃষি ক্যালেন্ডার:</Text> <Text>🗓️ জুলাই: রোপন, আগাছা নিয়ন্ত্রণ</Text> <Text>📌 আগস্ট: সার প্রয়োগ, রোগবালাই দেখা</Text> </View> ); }

// File: src/screens/CommunityScreen.js import React from 'react'; import { View, Text } from 'react-native';

export default function CommunityScreen() { return ( <View style={{ padding: 20 }}> <Text style={{ fontSize: 20 }}>কৃষক কমিউনিটি ফোরাম:</Text> <Text>👨‍🌾 রফিক: আমি BRRI-28 চাষ করছি, অভিজ্ঞতা ভালো</Text> <Text>👩‍🌾 রহিমা: আগাছা নিয়ন্ত্রণের সহজ উপায় আছে?</Text> </View> ); }

// File: src/screens/GovernmentSupportScreen.js import React from 'react'; import { View, Text } from 'react-native';

export default function GovernmentSupportScreen() { return ( <View style={{ padding: 20 }}> <Text style={{ fontSize: 20 }}>সরকারি সহায়তা:</Text> <Text>📢 কৃষি প্রণোদনা প্রকল্প</Text> <Text>💰 কৃষিঋণ পাওয়ার নিয়ম</Text> <Text>📝 সহজ রেজিস্ট্রেশন প্রক্রিয়া</Text> </View> ); }

// File: src/screens/OfflineContentScreen.js import React from 'react'; import { View, Text } from 'react-native';

export default function OfflineContentScreen() { return ( <View style={{ padding: 20 }}> <Text style={{ fontSize: 20 }}>অফলাইন তথ্য:</Text> <Text>📦 ইন্টারনেট ছাড়াও সংরক্ষিত তথ্য পড়া যাবে</Text> <Text>📖 মৌলিক গাইড, রোগ চিহ্ন, ক্যালেন্ডার অফলাইনে থাকবে</Text> </View> ); }

// File: src/screens/ImageHelpScreen.js import React from 'react'; import { View, Text, Image } from 'react-native';

export default function ImageHelpScreen() { return ( <View style={{ padding: 20 }}> <Text style={{ fontSize: 20 }}>ছবি তুলে রোগ শনাক্ত করুন (ডেমো)</Text> <Image source={{ uri: 'https://via.placeholder.com/150' }} style={{ height: 150, width: 150 }} /> <Text>📸 আপনার ফসলের ছবি তুলে আপলোড করুন</Text> <Text>🤖 এআই সিস্টেম রোগ শনাক্ত করতে সাহায্য করবে (ডেমো ভার্সন)</Text> </View> ); }
