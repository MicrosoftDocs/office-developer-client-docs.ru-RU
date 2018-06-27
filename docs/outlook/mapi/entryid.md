---
title: ИДЕНТИФИКАТОР ЗАПИСИ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ENTRYID
api_type:
- COM
ms.assetid: 8ebb21ca-5ad1-4dcc-97b6-2390664b5d8d
description: '���� ���������� ���������: 9 ����� 2015 �.'
ms.openlocfilehash: 1b55703c9ad12e3645e6e9cb3dcfcbdf21b90d25
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808385"
---
# <a name="entryid"></a>ИДЕНТИФИКАТОР ЗАПИСИ

  
  
**Применимо к**: Outlook 
  
Содержит идентификатор записи для объекта MAPI. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
|Связанные макросы:  <br/> |[CbNewENTRYID](cbnewentryid.md), [SizedENTRYID](sizedentryid.md) <br/> |
   
```cpp
typedef struct
{
  BYTE abFlags[4];
  BYTE ab[MAPI_DIM];
} ENTRYID, FAR *LPENTRYID;

```

## <a name="members"></a>Элементы

 **abFlags**
  
> Битовая маска флагов, предоставляющих сведения об объекте. Первого байта ответа флаги **abFlags [0]**, может задать поставщиком; другие три зарезервированы. Эти флаги не должны быть установлены для идентификаторов навсегда; они определены только для краткосрочных идентификаторы записей. Для клиентов эта структура доступен только для чтения. Можно задать следующие флаги в **abFlags [0]**:
    
MAPI_NOTRECIP 
  
> Идентификатор записи нельзя использовать в качестве получателей на сообщение.
    
MAPI_NOTRESERVED 
  
> Другие пользователи не могут получить доступ к идентификатор записи.
    
MAPI_NOW 
  
> Идентификатор записи не может использоваться в других случаях.
    
MAPI_SHORTTERM 
  
> Идентификатор записи краткосрочных. Все значения в этом байтов должно иметь значение, если не включены другие варианты использования идентификатор записи.
    
MAPI_THISSESSION 
  
> Идентификатор записи не может использоваться в других сеансов.
    
 **AB**
  
> Указывает массив двоичные данные, используемые поставщиками услуг. Клиентское приложение не может использовать этот массив.
    
## <a name="remarks"></a>Замечания

Структура **ENTRYID** используется сообщение хранения и адресной книги поставщиков для создания уникальных идентификаторов для объектов. Идентификаторы входа используются для определения следующих типов объектов: 
  
- Хранилищ сообщений
    
- Папки
    
- Сообщения
    
- Контейнеры адресной книги
    
- Списки рассылки
    
- Пользователи системы обмена сообщениями
    
- Объекты состояния
    
- Разделы профилей
    
Каждый поставщик использует формат для структуры **ENTRYID** , который имеет смысл для этого поставщика. 
  
Идентификаторы записей нельзя сравнивать напрямую, так как один объект могут быть представлены два двоичные значения. Чтобы определить, представляют ли два идентификаторы записей тот же объект, вызовите метод [IMAPISession::CompareEntryIDs](imapisession-compareentryids.md) . 
  
Когда клиент вызывает метод [IMAPIProp::GetProps](imapiprop-getprops.md) объекта для извлечения его идентификатор записи, объект возвращает наиболее постоянное формы идентификатор записи. Клиент может убедитесь, что идентификатор записи долгосрочного, проверьте, что ни один из флагов, заданы в первого байта ответа **abFlags** элемента. 
  
При обращении идентификатор записи через столбца в таблице, скорее всего, этот идентификатор записи краткосрочных вместо долгосрочного. Краткосрочные идентификаторы записей можно использовать для открытия их соответствующими объектами только во время текущего сеанса MAPI. Клиент может убедитесь, что идентификатор записи краткосрочных, проверьте, что все флажки, заданы в первого байта ответа **abFlags** элемента. 
  
Некоторые идентификаторы записей краткосрочной, но имеют длительного использования. Этот идентификатор записи будут иметь одно или несколько соответствующих набора флагов в первого байта ответа его **abFlags** элементом. 
  
Структуру **ENTRYID** напоминает структуру [FLATENTRY](flatentry.md) . Тем не менее существуют некоторые отличия: 
  
- Структуру **ENTRYID** не сохраняет размер идентификатор записи; выполняет **FLATENTRY** структуры. 
    
- Структуру **ENTRYID** хранит данные флаг и rest идентификатор записи отдельно; Структура **FLATENTRY** хранит данные флаг с помощью rest идентификатор записи. 
    
- Структуру **ENTRYID** передается как параметр для методов интерфейса [IMAPIProp](imapipropiunknown.md) и следующие методы **OpenEntry** : [IABLogon::OpenEntry](iablogon-openentry.md), [IAddrBook::OpenEntry](iaddrbook-openentry.md) [IMAPIContainer::OpenEntry ](imapicontainer-openentry.md), [IMAPISession::OpenEntry](imapisession-openentry.md), [IMAPISupport::OpenEntry](imapisupport-openentry.md), [IMsgStore::OpenEntry](imsgstore-openentry.md), [IMSLogon::OpenEntry](imslogon-openentry.md)
    
- Структура **ENTRYID** используется для хранения идентификатора записи на диск. Структура **FLATENTRY** используется для хранения идентификатора записи в файл или передайте его в виде потока в байтах. 
    
Клиенты всегда должен передавать идентификаторы естественно выровненные записей. Несмотря на то, что поставщики будут обрабатывать идентификаторы произвольно выровненные записей, клиенты не следует ожидать это поведение. Сбой, связанный с передавать идентификатор хорошим выровненным запись в метод может привести к сбою выравнивание на процессор RISC. 
  
Коэффициент природные выравнивание, обычно 8 байтов является большой тип данных, поддерживаемый ЦП и обычно же коэффициента выравнивание путем выделения памяти системы. Адрес естественно выровненные памяти позволяет ЦП для доступа к любой тип данных, поддерживаемых по этому адресу без создания ошибку выравнивание. Для ЦП RISC тип данных размером N байт должен обычно выравнивания на делится N байт с адреса, который делится N.
  
Для получения дополнительных сведений см [Идентификаторы записей](mapi-entry-identifiers.md). 
  
## <a name="see-also"></a>См. также



[FLATENTRY](flatentry.md)
  
[IMAPISupport::CompareEntryIDs](imapisupport-compareentryids.md)
  
[Каноническое свойство PidTagRecordKey](pidtagrecordkey-canonical-property.md)


[Структуры MAPI](mapi-structures.md)
