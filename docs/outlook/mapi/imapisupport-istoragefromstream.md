---
title: IMAPISupportIStorageFromStream
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.IStorageFromStream
api_type:
- COM
ms.assetid: da9e8fdc-dfc5-4ecc-9f9b-b76921b92d7c
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: a73c87f172b4c97379bb9cd117679d3947c188af
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809130"
---
# <a name="imapisupportistoragefromstream"></a>IMAPISupport::IStorageFromStream

  
  
**Относится к**: Outlook 
  
Реализует объект хранилища для доступа к потоку.
  
```cpp
HRESULT IStorageFromStream(
  LPUNKNOWN lpUnkIn,
  LPCIID lpInterface,
  ULONG ulFlags,
  LPSTORAGE FAR * lppStorageOut
);
```

## <a name="parameters"></a>Параметры

 _lpUnkIn_
  
> [in] Указатель на объект stream.
    
 _lpInterface_
  
> [in] Указатель на идентификатор интерфейса (ИД интерфейса), который представляет интерфейс, который будет использоваться для доступа к потоку, на который указывает _lpUnkIn_. Допустимы любые из следующих значений: IID_IStream, IID_ILockBytes, или **значение null**, это означает, что интерфейс [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx) должен использоваться для доступа к потоку. 
    
 _ulFlags_
  
> [in] Битовая маска флаги, который определяет, как должны создаваться по отношению к объекту потока объекта хранилища. По умолчанию хранение создается с доступом только для чтения и начинается поток в нулевой позиции в хранилище. Можно задать следующие флажки:
    
STGSTRM_CREATE 
  
> Следует создавать новый объект хранилища для объекта потока.
    
STGSTRM_CURRENT 
  
> Объект хранилища будет запускаться в текущей позиции потока.
    
STGSTRM_MODIFY 
  
> Вызывающего должны иметь разрешение на чтение и запись на объект возвращенные хранилища.
    
STGSTRM_RESET 
  
> Объект хранилища будет запускаться в нулевой позиции.
    
 _lppStorageOut_
  
> [out] Указатель на указатель на объект хранилища.
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> Объект хранилища успешно создан.
    
## <a name="remarks"></a>Замечания

Метод **IMAPISupport::IStorageFromStream** применяется для всех объектов поддержки поставщика службы. Поставщики услуг вызова **IStorageFromStream** для создания объекта хранилища для открытия отдельного свойства. Поставщики услуг, которые имеют собственные реализации интерфейса [IStorage](http://msdn.microsoft.com/en-us/library/aa380015%28VS.85%29.aspx) не нужно вызвать **IStorageFromStream**. 
  
Объекта хранилища, созданные **IStorageFromStream** вызывает метод [IUnknown::AddRef](http://msdn.microsoft.com/en-us/library/ms691379%28v=VS.85%29.aspx) поток для увеличения его счетчик ссылок и уменьшает счетчик после выхода хранилища. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

При вызове метода [IMAPIProp::OpenProperty](imapiprop-openproperty.md) одного из объектов для открытия свойства с помощью интерфейса **IStorage** выполните следующие задачи: 
  
1. Откройте объект потока с разрешением на чтение и запись для свойства.
    
2. Внутренне отмечайте потока свойство как объект хранилища.
    
3. Вызов **IStorageFromStream** для создания объекта хранилища. 
    
4. Возвращает указатель на объект хранилища.
    
Если реализовать дополнительные интерфейсы, использующие объекта хранилища, создайте объект, который является оболочкой объекта хранилища и реализуйте метод [IUnknown::QueryInterface](http://msdn.microsoft.com/en-us/library/ms682521%28v=VS.85%29.aspx) более высокого уровня. 
  
Не разрешать свойство так, чтобы открыть с помощью интерфейса **IStream** , если он был создан **IStorage**. С другой стороны не разрешать свойство так, чтобы открыть с помощью интерфейса **IStorage** , если он был создан **IStream**. 
  
Одно исключение допускается использование интерфейса **IStreamDocfile** для потоковой передачи объект хранилища из одного контейнера в другой, но идентификатор интерфейса IID_IStreamDocfile должен быть передан в **OpenProperty** метода _lpInterface _параметр. 
  
## <a name="see-also"></a>См. также



[IMAPIProp::OpenProperty](imapiprop-openproperty.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

