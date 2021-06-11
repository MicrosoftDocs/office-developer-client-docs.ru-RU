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
ms.openlocfilehash: 7200e7d226eb148fef094ab8540990644d2d4c99
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316590"
---
# <a name="imapisupportistoragefromstream"></a>IMAPISupport::IStorageFromStream

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Реализует объект хранения для доступа к потоку.
  
```cpp
HRESULT IStorageFromStream(
  LPUNKNOWN lpUnkIn,
  LPCIID lpInterface,
  ULONG ulFlags,
  LPSTORAGE FAR * lppStorageOut
);
```

## <a name="parameters"></a>Parameters

 _lpUnkIn_
  
> [in] Указатель на объект потока.
    
 _lpInterface_
  
> [in] Указатель на идентификатор интерфейса (IID), который представляет интерфейс, используемый для доступа к потоку, на который указывает _lpUnkIn._ Любое из следующих значений допустимо: IID_IStream, IID_ILockBytes или **null,** что указывает на то, что интерфейс [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) должен использоваться для доступа к потоку. 
    
 _ulFlags_
  
> [in] Немного флагов, которые контролируют, как должен создаваться объект хранилища по отношению к объекту потока. По умолчанию хранилище создается с доступом только для чтения, а поток начинается с нуля в хранилище. Можно установить следующие флаги:
    
STGSTRM_CREATE 
  
> Для объекта потока необходимо создать новый объект хранения.
    
STGSTRM_CURRENT 
  
> Объект хранилища должен начинаться с текущего положения потока.
    
STGSTRM_MODIFY 
  
> Вызываемая должна иметь разрешение на чтение и записи возвращаемого объекта хранения.
    
STGSTRM_RESET 
  
> Объект хранилища должен начинаться с нуля.
    
 _lppStorageOut_
  
> [вышел] Указатель на указатель на объект хранения.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Объект хранения был успешно создан.
    
## <a name="remarks"></a>Примечания

Метод **IMAPISupport::IStorageFromStream** реализован для всех объектов поддержки поставщика услуг. Поставщики услуг называют **IStorageFromStream** для создания объекта хранения, который будет использовать для открытия определенных свойств. Поставщикам услуг, которые имеют собственную реализацию интерфейса [IStorage,](https://msdn.microsoft.com/library/aa380015%28VS.85%29.aspx) не нужно вызывать **IStorageFromStream.** 
  
Объект хранения, созданный **IStorageFromStream,** вызывает метод [IUnknown::AddRef,](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) чтобы прибавить количество ссылок, а затем приумножает количество, когда хранилище будет выпущено. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Когда [метод IMAPIProp::OpenProperty](imapiprop-openproperty.md) одного из объектов вызван для открытия свойства с интерфейсом **IStorage,** выполните следующие задачи: 
  
1. Откройте объект потока с разрешением чтения и записи для свойства.
    
2. Внутренне пометить поток свойств как объект хранилища.
    
3. Вызов **IStorageFromStream для** создания объекта хранения. 
    
4. Верни указатель этому объекту хранения.
    
Если вы реализуете дополнительные интерфейсы, которые используют объект хранения, создайте объект, который заворачивает объект хранилища, и реализуйте метод [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) более высокого уровня. 
  
Не разрешайте открывать свойство с интерфейсом **IStream,** если оно создано **с помощью IStorage.** И наоборот, не разрешайте открывать свойство с интерфейсом **IStorage,** если оно создано **с помощью IStream.** 
  
За одним исключением можно использовать интерфейс **IStreamDocfile** для потоковой передачи объекта хранения из одного контейнера в другой, но идентификатор интерфейса IID_IStreamDocfile должен быть передан в _параметре lpInterface_ метода **OpenProperty.** 
  
## <a name="see-also"></a>См. также



[IMAPIProp::OpenProperty](imapiprop-openproperty.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

