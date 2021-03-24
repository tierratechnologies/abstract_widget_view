# abstract_widget_view

A WidgetViewController pattern for separation of concerns




## IntelliJ - Live Templates

    1) Generate a new WidgetControllerView group - `wcv`

    class $NAME$ extends StatefulWidget {
      @override
      _$NAME$Controller createState() => _$NAME$Controller();
    }

    class _$NAME$Controller extends State<$NAME$> {
      @override
      Widget build(BuildContext context) => _$NAME$View(this);
    }

    class _$NAME$View extends WidgetView<$NAME$, _$NAME$Controller> {
      _$NAME$View(_$NAME$Controller state) : super(state);
    @override
      Widget build(BuildContext context) {
        return Container($END$);
      }
    }


    2) Generate a new WidgetView that is related to an existing Controller - `wv`
    class $NAME$View extends WidgetView<$T1$, $T2$>{
      const $NAME$View ($T2$ state, {Key key}) : super(state, key: key);

      @override
      Widget build(BuildContext context){
        return $END$
      }
    }