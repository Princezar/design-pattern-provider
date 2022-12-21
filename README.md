# design-pattern-provider
Provider design pattern explain

#Provider Sample 1
Model Class

class Name 
{
    String text;
}

class Age 
{
int number;
}

#Multiple Provider

MultiProvider(
    providers: [
        Provider<Name>(create: (_) => Name('Haris')),
        Provider<Age>(create: (_) => Age(22)),
    ],
    child: Home(),)


#Access Provider in Home Widgets
Home Widget

@override


Widget build(BuildContext context) 
{
    final name = Provider.of<Name>(context).text;
}

