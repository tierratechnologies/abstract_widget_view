# abstract_widget_view

A WidgetViewController pattern for separation of concerns




## IntelliJ - Live Templates

    1) Generate a new WidgetControllerView group - `wcv`

    class $NAME$ extends StatefulWidget {
      @override
      $NAME$Controller createState() => $NAME$Controller();
    }

    class $NAME$Controller extends State<$NAME$> {
      @override
      Widget build(BuildContext context) => $NAME$View(this);
    }

    class $NAME$View extends WidgetView<$NAME$, $NAME$Controller> {
      $NAME$View($NAME$Controller state) : super(state);
    @override
      Widget build(BuildContext context) {
        return Container($END$);
      }
    }


    2) Generate a new WidgetView that is related to an existing Controller - `wv`
    class $NAME$View extends WidgetView<$T1$, $T2$>{
      const $NAME$View ($T2$ state, {super.key}) : super(state);

      @override
      Widget build(BuildContext context){
        return $END$
      }
    }
