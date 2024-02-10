# Declarative UI Nedir?

Declarative UI, kullanıcı arayüzünü tanımlamak için programlamada bir yaklaşımı ifade eder. Bu yaklaşım, bir arayüzün nasıl görüneceğini ve davranacağını belirtirken, arka plandaki işlevselliği ayrıntılı olarak programlamak yerine, ne istendiğini açıkça ifade eder.

## Özellikler ve Avantajlar

- **Daha Kolay Anlaşılabilirlik:** Declarative UI, arayüzü açık bir şekilde tanımlar, bu da kodun daha okunabilir ve anlaşılabilir olmasını sağlar. Bu, yeni geliştiricilerin projeye daha hızlı adapte olmasını sağlar.

- **Daha Az Hata:** Geleneksel, işlevsel veya nesne yönelimli yaklaşımların aksine, Declarative UI, daha az kod yazmanızı gerektirir ve bu da daha az hata yapma olasılığını artırır.

- **Daha Fazla Esneklik:** Declarative UI, arayüzü nasıl oluşturacağınıza dair daha fazla esneklik sağlar. Bu, farklı cihazlara veya ekran boyutlarına uyum sağlamayı kolaylaştırır.

- **Hızlı Geliştirme:** Genellikle, Declarative UI kullanarak arayüzler oluşturmak, geleneksel yaklaşımlara göre daha hızlıdır. Bu, geliştirme sürecini hızlandırabilir ve zaman maliyetini azaltabilir.

## Dikkat Edilmesi Gereken Noktalar

- **Tamamen Declarative Olmayabilir:** Bir arayüzü tamamen Declarative UI ile tasarlamak her zaman mümkün olmayabilir. Bazı durumlarda, dinamik davranışlar veya veri manipülasyonu gibi işlevselliği sağlamak için bir miktar işlevsel veya nesne yönelimli kod yazmanız gerekebilir.

- **Performans İzleme:** Declarative UI çerçeveleri veya kütüphaneleri, bazen performans açısından optimize edilmemiş olabilir. Bu nedenle, büyük ve karmaşık arayüzlerde performansı izlemek ve gerektiğinde iyileştirmek önemlidir.

- **Kütüphane Seçimi:** Birçok farklı Declarative UI çözümü vardır (React, Vue.js, Angular gibi). Projenizin gereksinimlerine en uygun olanını seçmek önemlidir.



- # Declarative UI Örneği: Todo Listesi

Bu proje, basit bir todo listesi uygulamasını React kullanarak nasıl oluşturacağınızı göstermektedir.

## Özellikler

- Kullanıcılar yeni bir todo ekleyebilir.
- Eklenen todolar listelenir.
- Kullanıcılar ekledikleri todoları silebilir.

## Nasıl Kullanılır

1. Proje dizinine gidin.
2. `npm install` komutunu kullanarak gerekli paketleri yükleyin.
3. `npm start` komutunu kullanarak uygulamayı başlatın.
4. Tarayıcınızda `http://localhost:3000` adresine gidin ve uygulamayı görüntüleyin.

## Teknolojiler

Bu proje aşağıdaki teknolojileri kullanmaktadır:

- React
- JSX
- JavaScript

## Örnek Kod

```jsx
import React, { useState } from 'react';

function TodoList() {
  const [todos, setTodos] = useState([]);
  const [inputValue, setInputValue] = useState('');

  const handleInputChange = (e) => {
    setInputValue(e.target.value);
  };

  const handleAddTodo = () => {
    if (inputValue.trim() !== '') {
      setTodos([...todos, inputValue]);
      setInputValue('');
    }
  };

  const handleDeleteTodo = (index) => {
    const newTodos = todos.filter((_, i) => i !== index);
    setTodos(newTodos);
  };

  return (
    <div>
      <h1>Todo List</h1>
      <input 
        type="text" 
        value={inputValue} 
        onChange={handleInputChange} 
        placeholder="Enter a new todo" 
      />
      <button onClick={handleAddTodo}>Add Todo</button>
      <ul>
        {todos.map((todo, index) => (
          <li key={index}>
            {todo}
            <button onClick={() => handleDeleteTodo(index)}>Delete</button>
          </li>
        ))}
      </ul>
    </div>
  );
}

export default TodoList;
```

# Deklaratif Olarak Düşünme ve React'te Uygulama


### Componentinizin Farklı Görsel Durumlarını Belirleyin

### Bu State Değişikliklerini Tetikleyen Unsurları Belirleyin

### Durumu useState ile Bellekte Temsil Edin

### Gereksiz Olan State Değişkenlerini Kaldırın

### Stateleri ayarlamak için etkinlik dinleyiciler(Event handlers) kullanın ve State durumlarını güncelleyin, yenileyin, kontrol edin.


Bu adımları takip ederek, React'te deklaratif bir yaklaşımla UI'yi nasıl uygulayabileceğinizi daha iyi anlayacaksınız.



