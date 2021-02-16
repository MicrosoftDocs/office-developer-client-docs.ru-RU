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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
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
  
> [in] Указатель на идентификатор интерфейса (IID), который представляет интерфейс, используемый для доступа к потоку, на который указывает _lpUnkIn._ Допустимы любые из следующих значений: IID_IStream, IID_ILockBytes **или null,** что означает, что интерфейс [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) должен использоваться для доступа к потоку. 
    
 _ulFlags_
  
> [in] Битоваяmas флагов, которая управляет тем, как создается объект хранилища относительно объекта stream. По умолчанию хранилище создается с доступом только для чтения, а поток начинается с нуля в хранилище. Можно установить следующие флаги:
    
STGSTRM_CREATE 
  
> Для объекта stream необходимо создать новый объект хранилища.
    
STGSTRM_CURRENT 
  
> Объект хранилища должен начинаться с текущего положения потока.
    
STGSTRM_MODIFY 
  
> Вызываемая должна иметь разрешение на чтение и записи для возвращенного объекта хранилища.
    
STGSTRM_RESET 
  
> Объект хранилища должен начинаться с нуля.
    
 _lppStorageOut_
  
> [out] Указатель на указатель на объект хранилища.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Объект хранилища успешно создан.
    
## <a name="remarks"></a>Примечания

Метод **IMAPISupport::IStorageFromStream** реализован для всех объектов поддержки поставщика услуг. Поставщики услуг вызовите **IStorageFromStream,** чтобы создать объект хранилища, который будет применяться для открытия определенных свойств. Поставщикам услуг, которые имеют собственную реализацию [интерфейса IStorage,](https://msdn.microsoft.com/library/aa380015%28VS.85%29.aspx) не требуется вызывать **IStorageFromStream.** 
  
Объект хранилища, созданный **IStorageFromStream,** вызывает метод [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) потока для инкрементного подсчета ссылок, а затем при отпущении хранилища понижается. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

При [выполнении метода IMAPIProp::OpenProperty](imapiprop-openproperty.md) одного из ваших объектов для открытия свойства с помощью интерфейса **IStorage** выполните следующие задачи: 
  
1. Откройте объект stream с разрешением на чтение и записи для свойства.
    
2. Внутренне пометить поток свойств как объект хранилища.
    
3. Вызовите **IStorageFromStream для** создания объекта хранилища. 
    
4. Возвращает указатель на этот объект хранилища.
    
При реализации дополнительных интерфейсов, которые используют объект хранилища, создайте объект, который будет обтекать объект хранилища, и реализуйте метод [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) более высокого уровня. 
  
Не разрешайте открывать свойство с помощью **интерфейса IStream,** если оно было создано с помощью **IStorage.** И наоборот, не разрешайте открывать свойство с помощью **интерфейса IStorage,** если оно было создано с **помощью IStream.** 
  
За одним исключением, можно использовать интерфейс **IStreamDocfile** для потоковой передачи объекта хранилища из одного контейнера в другой, но идентификатор интерфейса IID_IStreamDocfile должен быть передан в _параметре lpInterface_ метода **OpenProperty.** 
  
## <a name="see-also"></a>См. также



[IMAPIProp::OpenProperty](imapiprop-openproperty.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

