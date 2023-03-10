## Behavior 
	guarda um valor a devolver quando ha o evento
## Dynamic
	função que muda um Behaviour quando ocorre um Event
## Event   
	dispara quando ha uma cação, Click, Input...

## ob init
## ob run
## ob hoogle
    Run a hoogle server locally for your project's dependency tree

# Funções que fui recolhendo
Para informações mais de tudo usar a [[Reflex-Quick-Reference]] que tem todas as funções do [Reflex](https://reflex-frp.org/get-started)

## data Dynamic t :: * -> *
    A container for a value that can change over time and allows
    notifications on changes. Basically a combination of a Behavior and
    an Event, with a rule that the Behavior will change if and only if
    the Event fires.

## data Event t :: * -> *
    A stream of occurrences. During any given frame, an Event is either
    occurring or not occurring; if it is occurring, it will contain a
    value of the given type (its "occurrence type")

## data Behavior t :: * -> *
    A container for a value that can change over time. Behaviors can
    be sampled at will, but it is not possible to be notified when
    they change


### holdDyn :: a -> Event t a -> m (Dynamic t a)
    Create a Dynamic value using the given initial value that changes
    every time the Event occurs.

### updated :: Dynamic t a -> Event t a
    Extract the Event of the Dynamic.

### elDynAttr :: Text -> Dynamic t (Map Text Text) -> m a -> m a
    Create a DOM element with Dynamic Attributes


### mergeWith :: (a -> a -> a) -> [Event t a] -> Event t a
    Create a new Event that occurs if at least one of the Events in the list occurs. If multiple occur at the same time they are folded from the left with the given function.

### accumDyn ::  (a -> b -> a) -> a -> Event t b -> m (Dynamic t a)
    Accumulate a Dynamic by folding occurrences of an Event with the provided function. See foldDyn.

### count :: Event t a -> m (Dynamic t b)
    Create a new Dynamic that counts the occurrences of the Event.



### headE :: Event t a -> m (Event t a)
    Create a new Event that only occurs only once, on the first occurrence of the supplied Event.

### tailE :: Event t a -> m (Event t a)
    Create a new Event that occurs on all but the first occurrence of the supplied Event.

### constant :: a -> Behavior t a
    Create a Behavior that always has the given value

### never :: Event t a
    An Event with no occurrences

### gate :: Behavior t Bool -> Event t a -> Event t a
    Create a new Event that only occurs if the supplied Event occurs and the Behavior is true at the time of occurrence.

### toggle ::  Bool -> Event t a -> m (Dynamic t Bool)
    Create a new Dynamic using the initial value that flips its value every time the Event occurs.



### switchHold :: Event t a -> Event t (Event t a) -> m (Event t a)
    Switches to the new event whenever it receives one. Only the old event is considered the moment a new one is switched in; the output event will fire at that moment only if the old event does.

### current :: Dynamic t a -> Behavior t a
    Extract the Behavior of a Dynamic.

---
Status:
#cheat-sheets
Tags: [[Programming]]