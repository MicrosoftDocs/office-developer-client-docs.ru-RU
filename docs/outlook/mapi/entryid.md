---
title: ENTRYID
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
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: c77acb5226361ce31a7f6b1694de7fe23f8dd71b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415273"
---
# <a name="entryid"></a>ENTRYID

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит идентификатор входа для объекта MAPI. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
|Связанные макрос:  <br/> |[CbNewENTRYID](cbnewentryid.md), [SizedENTRYID](sizedentryid.md) <br/> |
   
```cpp
typedef struct
{
  BYTE abFlags[4];
  BYTE ab[MAPI_DIM];
} ENTRYID, FAR *LPENTRYID;

```

## <a name="members"></a>"Участники"

 **abFlags**
  
> Bitmask флагов, которые предоставляют информацию, которая описывает объект. Поставщик может установить только первый набор **флагов, abFlags[0];** остальные три зарезервированы. Эти флаги не должны устанавливаться для идентификаторов постоянных записей; они устанавливаются только для краткосрочных идентификаторов записей. Для клиентов эта структура является только для чтения. Следующие флаги можно установить в **abFlags[0]**:
    
MAPI_NOTRECIP 
  
> Идентификатор записи не может использоваться в качестве получателя в сообщении.
    
MAPI_NOTRESERVED 
  
> Другие пользователи не могут получить доступ к идентификатору записи.
    
MAPI_NOW 
  
> Идентификатор записи не может использоваться в другое время.
    
MAPI_SHORTTERM 
  
> Идентификатор записи является краткосрочным. Все другие значения в этом byte должны быть заданной, если не включено другое использование идентификатора записи.
    
MAPI_THISSESSION 
  
> Идентификатор записи нельзя использовать на других сеансах.
    
 **ab**
  
> Указывает массив двоичных данных, используемых поставщиками услуг. Клиентские приложения не могут использовать этот массив.
    
## <a name="remarks"></a>Примечания

Структура **ENTRYID** используется поставщиками сообщений и адресных книг для создания уникальных идентификаторов для своих объектов. Идентификаторы записей используются для определения следующих типов объектов: 
  
- Хранилища сообщений
    
- Folders
    
- Сообщения
    
- Контейнеры адресной книги
    
- Списки рассылки
    
- Пользователи обмена сообщениями
    
- Объекты состояний
    
- Разделы профилей
    
Каждый поставщик использует формат **структуры ENTRYID,** который имеет смысл для этого поставщика. 
  
Идентификаторы записи нельзя сравнивать напрямую, так как один объект может быть представлен двумя разными двоичными значениями. Чтобы определить, представляют ли два идентификатора записи один и тот же объект, позвоните по методу [IMAPISession::CompareEntryIDs.](imapisession-compareentryids.md) 
  
Когда клиент вызывает метод [IMAPIProp::GetProps](imapiprop-getprops.md) объекта для получения его идентификатора входа, объект возвращает самую постоянную форму идентификатора записи. Клиент может убедиться, что идентификатор записи является долгосрочным, проверяя, что ни один из флагов не установлен в первой части **участника abFlags.** 
  
Если клиент получает доступ к идентификатору записи через столбец в таблице, скорее всего, этот идентификатор записи является краткосрочным, а не долгосрочным. Краткосрочные идентификаторы записи можно использовать для открытия соответствующих объектов только в текущем сеансе MAPI. Клиент может убедиться, что идентификатор записи является краткосрочным, проверяя, что все флаги задают в первой части **участника abFlags.** 
  
Некоторые идентификаторы записей являются краткосрочными, но имеют долгосрочное использование. Такой идентификатор записи будет иметь один или несколько соответствующих флагов, установленных в первом byte своего **члена abFlags.** 
  
Структура **ENTRYID** напоминает структуру [FLATENTRY.](flatentry.md) Однако существуют некоторые различия: 
  
- Структура **ENTRYID** не сохраняет размер идентификатора записи; структура **FLATENTRY.** 
    
- Структура **ENTRYID** хранит данные флага и остальные идентификаторы входа отдельно; структура **FLATENTRY** хранит данные флага с остальным идентификатором записи. 
    
- Структура **ENTRYID** передается в качестве параметра методам интерфейса [IMAPIProp](imapipropiunknown.md) и следующим методам **OpenEntry:** [IABLogon::OpenEntry,](iablogon-openentry.md) [IAddrBook::OpenEntry,](iaddrbook-openentry.md) [IMAPIContainer::OpenEntry,](imapicontainer-openentry.md) [IMAPISession::OpenEntry,](imapisession-openentry.md) [IMAPISupport::OpenEntry](imapisupport-openentry.md), [IMsgStore::OpenEntry](imsgstore-openentry.md), [IMSLogon:OpenEntry](imslogon-openentry.md)
    
- Структура **ENTRYID** используется для хранения идентификатора записи на диске. Структура **FLATENTRY** используется для хранения идентификатора записи в файле или передачи его в потоке bytes. 
    
Клиенты всегда должны проходить в естественно выровненных идентификаторах записей. Хотя поставщики должны обрабатывать произвольно выровненные идентификаторы записей, клиенты не должны ожидать такого поведения. Невыполнение правильного идентификатора входа в метод может привести к сбою выравнивания на процессорах RISC. 
  
Естественный коэффициент выравнивания, обычно 8 bytes, это самый большой тип данных, поддерживаемый ЦП, и, как правило, тот же фактор выравнивания, используемый в системе памяти. Естественно выровненный адрес памяти позволяет ЦП получать доступ к любому типу данных, который он поддерживает по этому адресу, без создания ошибки выравнивания. Для ЦП RISC тип данных размером N-bytes обычно должен выравниваться по даже нескольким N-bytes, при этом адрес является даже нескольким N.
  
Дополнительные сведения см. в [документе Entry Identifiers](mapi-entry-identifiers.md). 
  
## <a name="see-also"></a>См. также



[FLATENTRY](flatentry.md)
  
[IMAPISupport::CompareEntryIDs](imapisupport-compareentryids.md)
  
[Каноническое свойство PidTagRecordKey](pidtagrecordkey-canonical-property.md)


[Структуры MAPI](mapi-structures.md)

