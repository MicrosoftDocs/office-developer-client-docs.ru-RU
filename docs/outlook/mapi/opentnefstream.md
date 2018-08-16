---
title: OpenTnefStream
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.OpenTnefStream
api_type:
- COM
ms.assetid: 912d7799-53ce-42a7-9fbd-f9a6a3a56047
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 866d3be5e1c7a4375db84d1f15802e01f8d10f23
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810073"
---
# <a name="opentnefstream"></a>OpenTnefStream

**Относится к**: Outlook 
  
Вызывается с помощью поставщика транспорта для запуска сеанса MAPI транспорта Neutral Encapsulation формата TNEF. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |TNEF.h  <br/> |
|Реализованный:  <br/> |MAPI  <br/> |
|Вызывается:  <br/> |Поставщиками транспорта  <br/> |
   
```cpp
HRESULT OpenTnefStream(
  LPVOID lpvSupport,
  LPSTREAM lpStream,
  LPSTR lpszStreamName, 
  ULONG ulFlags,
  LPMESSAGE lpMessage,
  WORD wKey,
  LPITNEF FAR * lppTNEF
);
```

## <a name="parameters"></a>Параметры

_lpvSupport_
  
> [in] Передает объект поддержки или передает значение NULL. 
    
_lpStream_
  
> [in] Указатель на хранилище потока объекта OLE **IStream** интерфейс предоставление источника и назначения для потока сообщения в формате TNEF. 
    
_lpszStreamName_
  
> [in] Указатель на имя потока данных, который использует объект TNEF. Если вызывающего абонента есть флаг TNEF_ENCODE (параметр _ulFlags_ ) в своем вызове **OpenTnefStream**, параметр _lpszName_ необходимо указать ненулевое указатель строка ненулевое, состоящая из произвольных символов, допустимом для задания имени файла. MAPI не разрешает строковые имена, включая символы «[», «]», или «:», даже если в файловой системе разрешает их использования. Размер строки, переданное для _lpszName_ не должно превышать значение MAX_PATH, максимальная длина строка, содержащая имя пути. 
    
_ulFlags_
  
> [in] Битовая маска флаги служит для указания режима функции. Можно задать следующие флажки:
    
TNEF_BEST_DATA 
  
> Все возможные свойства сопоставляются их атрибутов нижнего уровня, но если потери данных из-за преобразования с атрибутом нижнего уровня, свойство также кодируются в encapsulations. Обратите внимание на то, что это приведет к повторяющихся данных в поток TNEF. Если не указаны не другие режимы TNEF_BEST_DATA значение по умолчанию. 
    
TNEF_COMPATIBILITY 
  
> Обеспечивает обратную совместимость с более старые клиентского приложения. Потоки TNEF в кодировке этот флаг будут сопоставлены с все возможные свойства их соответствующий атрибут нижнего уровня. Этот режим вызывает по умолчанию некоторые свойства, необходимых для клиентов более ранних версий. 
    
  > [!CAUTION]
  > Этот флаг устарел и не должен использоваться. 
  
TNEF_DECODE 
  
> Объект TNEF в указанном потоке открывается с доступом только для чтения. Поставщика транспорта необходимо установить этот флаг, если он хочет функции для инициализации объекта для последующих декодирования.
    
TNEF_ENCODE 
  
> Объект TNEF в указанном потоке открывается для разрешения на чтение и запись. Поставщика транспорта необходимо установить этот флаг, если он хочет функции для инициализации объекта для последующих кодировки.
    
TNEF_PURE 
  
> Кодирует все свойства в блоки инкапсуляция MAPI. Таким образом, файл «чистая» TNEF будет состоять из, в большинстве, attMAPIProps attAttachment, attRenddata и attRecipTable. Этот режим идеально подходит для использования при необходимости без обратной совместимости.
    
_lpMessage_
  
> [in] Указатель на объект сообщения как место назначения для декодированное сообщения с вложениями или источника для закодированного сообщения с вложениями. Любые свойства назначения сообщения могут быть перезаписаны по свойствам закодированное сообщение.
    
_wKey_
  
> [in] Клавиша поиска, который использует объект TNEF в соответствии с вложениями в теги текст, вставленный в качестве текста сообщения. Это значение должно быть относительно уникальным для сообщений.
    
_lppTNEF_
  
> [out] Указатель на новый объект TNEF.
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
## <a name="remarks"></a>���������

Объект TNEF, созданных функцией **OpenTnefStream** позднее вызывает метод OLE **IUnknown::AddRef** для добавления ссылки на объект поддержки, объект stream и объект message. Поставщика транспорта можно удалить ссылки для всех трех объектов с помощью одного вызова метода OLE **функции IUnknown::Release** на объекте TNEF. 
  
**OpenTnefStream** выделяет и инициализирует интерфейсом **ITnef** объект TNEF для поставщика для использования в кодировке **IMessage** интерфейсом MAPI сообщения в сообщения в формате TNEF потока. Кроме того функции можно задать объект для поставщика для использования в последующих вызовов [ITnef::ExtractProps](itnef-extractprops.md) для декодирования сообщения в формате TNEF потока в сообщение MAPI. Чтобы закрыть сеанс освобождения объекта TNEF, поставщика транспорта необходимо вызвать метод унаследованные **функции IUnknown::Release** на объекте. 
  
Эта функция — это исходное точки входа для доступа к TNEF и вместо нее [OpenTnefStreamEx](opentnefstreamex.md) , но по-прежнему используется для обеспечения совместимости для тех, кто уже использует TNEF. 
  
## <a name="see-also"></a>См. также

- [IMAPISupport: IUnknown](imapisupportiunknown.md)
- [IXPProvider::TransportLogon](ixpprovider-transportlogon.md)
