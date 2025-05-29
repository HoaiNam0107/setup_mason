- step 1: mason init

- step 2: mason new clean_architecture_feature

- step 3: create __brick__/lib/

__brick__/lib/
├── data/
│   ├── models/{{feature_name}}_model.dart
│   ├── repositories/{{feature_name}}_repository_impl.dart
│   └── sources/
│       ├── local/{{feature_name}}_local_datasource.dart
│       └── remote/{{feature_name}}_remote_datasource.dart
├── domain/
│   ├── entities/{{feature_name}}.dart
│   ├── repositories/{{feature_name}}_repository.dart
│   └── usecases/{{feature_name}}_usecase.dart
├── presentation/
│   ├── blocs/{{feature_name}}_bloc/
│   │   ├── {{feature_name}}_bloc.dart
│   │   ├── {{feature_name}}_event.dart
│   │   └── {{feature_name}}_state.dart
│   ├── screens/{{feature_name}}_screen.dart
│   └── widgets/{{feature_name}}_button.dart


- step 4: update brick.yaml

name: clean_architecture_feature
description: A brick to generate a Clean Architecture feature for Flutter
version: 0.1.0+1
vars:
feature_name:
type: string
description: The name of the feature (e.g., login, user_profile)
prompt: Enter the feature name (snake_case)

- step 5: register brick in mason.yaml

bricks:
clean_architecture_feature:
path: ./clean_architecture_feature

mason get

- step 6: 

mason make clean_architecture_feature --feature_name login_google

mason update 