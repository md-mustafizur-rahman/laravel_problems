If we want to deploy laravel brezze and jetstream css / tailwind css with proper style

then we have to remove :

        @vite(['resources/css/app.css', 'resources/js/app.js'])

temporary solution:


  <link rel="stylesheet" href="{{ asset('css/app.css') }}">
<script src="{{ asset('js/app.js') }}" defer></script>
         <script src="https://cdn.tailwindcss.com"></script>
 <script src="https://cdn.tailwindcss.com"></script>


 final solution:
after npm run build add link the app and app.blade.php , guest.blade.php on the breeze or jetstream layout

 <link rel="stylesheet" href="{{url('build/assets/app-e12641bb.css')}}" />
<script src="{{url('build/assets/app-7c0572f8.js')}}"></script>
    
