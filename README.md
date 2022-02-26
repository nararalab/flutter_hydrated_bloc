# flutter_hydrated_bloc

플루터 하이드레이티드 블락

## 프로젝트 설명

증가된 카운트 값을 저장하여, 앱이 재시작 되었을때도, 그 값을 유지함.

### 앱실행전, 스토리지 처리

```dart
void main() async {
  WidgetsFlutterBinding.ensureInitialized();
  final storage = await HydratedStorage.build(
    storageDirectory: await getApplicationDocumentsDirectory(),
  );
  HydratedBlocOverrides.runZoned(
    () => runApp(const MyApp()),
    storage: storage,
  );
}
```

## Dependencies

```bash
flutter pub add equatable
flutter pub add flutter_bloc
flutter pub add hydrated_bloc
flutter pub add path_provider
```
