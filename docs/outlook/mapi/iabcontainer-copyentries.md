---
title: IABContainerCopyEntries
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABContainer.CopyEntries
api_type:
- COM
ms.assetid: 4e775228-5ceb-4002-9b68-999fb5889b86
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: ddb730ed92db4c8d281e7c8d5d9b18bc44505598
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346398"
---
# <a name="iabcontainercopyentries"></a>IABContainer::CopyEntries

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Копирует одну или несколько записей, как правило, для обмена сообщениями с пользователями или списками рассылки.
  
```cpp
HRESULT CopyEntries(
  LPENTRYLIST lpEntries,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Параметры

 _lpEntries_
  
> [in] Указатель на массив структур [ENTRYLIST,](entrylist.md) содержащий идентификаторы записей для копирования. 
    
 _ulUIParam_
  
> [in] Handle to the parent window of any dialog boxes or windows that this method displays. Параметр _ulUIParam_ должен быть нулем, если AB_NO_DIALOG флага в _параметре ulFlags._ 
    
 _lpProgress_
  
> [in] Указатель на объект хода выполнения, отображает индикатор хода выполнения или NULL. Если _lpProgress_ имеет NULL, индикатор хода выполнения должен отображаться с помощью объекта хода выполнения, предоставленного MAPI с помощью метода [IMAPISupport::D oProgressDialog.](imapisupport-doprogressdialog.md) Параметр _lpProgress_ игнорируется, если флаг AB_NO_DIALOG установлен в _ulFlags._
    
 _ulFlags_
  
> [in] Битоваяmas флагов, которая управляет выполнением операции копирования. Можно установить следующие флаги:
    
AB_NO_DIALOG 
  
> Подавляет отображение индикатора хода выполнения. Если этот флаг не установлен, отображается индикатор хода выполнения.
    
CREATE_CHECK_DUP_LOOSE 
  
> Указывает на то, что должен выполняться свободный уровень проверки дублирующихся записей. Реализация свободной проверки записей является конкретной для поставщика. Например, поставщик может определить свободное совпадение как любые две записи с одинаковым отображаемой именем.
    
CREATE_CHECK_DUP_STRICT 
  
> Указывает, что необходимо выполнять строгий уровень проверки записей. Реализация строгой проверки дубликатов записей является конкретной для поставщика. Например, поставщик может определить строгое соответствие как любые две записи с одинаковым отображаемого имени и адресом обмена сообщениями.
    
CREATE_REPLACE 
  
> Указывает, что новая запись должна заменить существующую, если определено, что эти две записи являются дубликатами.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Операция копирования была успешной.
    
MAPI_W_PARTIAL_COMPLETION 
  
> Операция копирования в целом прошла успешно, но не удалось скопировать одну или несколько записей. При возвращении этого значения вызов должен быть обработан как успешный. Чтобы проверить это значение,  используйте HR_FAILED макрос. Дополнительные сведения см. в [теме "Использование макроса для обработки ошибок".](using-macros-for-error-handling.md)
    
## <a name="remarks"></a>Примечания

Метод **IABContainer::CopyEntries** копирует записи из одного или другого контейнера. Вызов **CopyEntries функционально эквивалентен** следующим вызовам для копирования каждой записи: 
  
1. Метод [IABContainer::CreateEntry](iabcontainer-createentry.md) для создания новой записи. 
    
2. Метод [IMAPIProp::GetProps](imapiprop-getprops.md) для чтения свойств из записи для копирования. 
    
3. Метод [IMAPIProp::SetProps](imapiprop-setprops.md) для записи свойств в новую запись. 
    
4. Метод [IMAPIProp::SaveChanges](imapiprop-savechanges.md) новой записи для сохранения. 
    
5. Метод [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28VS.85%29.aspx) новой записи для освобождения ссылки контейнера. 
    
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Все контейнеры, которые поддерживают метод **IABContainer::CopyEntries,** должны быть модификуемыми. Задайте флаг AB_MODIFIABLE контейнера в свойстве **PR_CONTAINER_FLAGS** ([PidTagContainerFlags),](pidtagcontainerflags-canonical-property.md)чтобы указать, что его можно модификатировать. 
  
Необходимо поддерживать все флаги; однако интерпретация и использование этих флагов специфитична для реализации, то есть вы можете определить, что означают семантика флагов CREATE_CHECK_DUP_LOOSE и CREATE_CHECK_DUP_STRICT в контексте реализации. Если вы не можете определить, является ли запись дубликатом, всегда разрешайте ее копирование. 
  
Если установлен CREATE_REPLACE, всегда копируйте запись независимо от того, CREATE_CHECK_DUP_LOOSE или CREATE_CHECK_DUP_STRICT установлен и является ли запись дубликатом. 
  
Если CREATE_REPLACE не установлен и CREATE_CHECK_DUP_STRICT установлен, проверьте, нет ли дубликатов. Если запись определена как дублирующаяся, не копируйте ее. 
  
Нет необходимости поддерживать CREATE_REPLACE; Не поддерживающие CREATE_REPLACE означает, что вы можете игнорировать его и всегда выполнять копирование. 
  
Возвращает предупреждение MAPI_W_PARTIAL_COMPLETION только в том случае, если недипликированная запись не может быть скопирована. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Используйте флаги CREATE_CHECK_DUP_LOOSE CREATE_CHECK_DUP_STRICT, чтобы указать поставщику, как контейнер должен выполнять проверку дубликатов записей. Если требуется добавить запись независимо от того, является ли она дубликатом, не устанавливая ни один из этих флагов, ни CREATE_REPLACE флага. CREATE_REPLACE указывает, что вам все равно, является ли запись дублирующейся; вы всегда хотите заменить исходную запись. 
  
## <a name="see-also"></a>См. также



[ENTRYLIST](entrylist.md)
  
[IABContainer::CreateEntry](iabcontainer-createentry.md)
  
[IMAPIProgress : IUnknown](imapiprogressiunknown.md)
  
[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[IABContainer : IMAPIContainer](iabcontainerimapicontainer.md)

