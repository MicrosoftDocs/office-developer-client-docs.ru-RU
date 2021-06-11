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

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Копирует одну или несколько записей, как правило, пользователей сообщений или списки рассылки.
  
```cpp
HRESULT CopyEntries(
  LPENTRYLIST lpEntries,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parameters

 _lpEntries_
  
> [in] Указатель на массив структур [ENTRYLIST,](entrylist.md) содержащий идентификаторы записей для копирования. 
    
 _ulUIParam_
  
> [in] Ручка родительского окна любых диалогов или окон, отображаемого этим методом. Параметр _ulUIParam_ должен быть нулем, если флаг AB_NO_DIALOG в _параметре ulFlags._ 
    
 _lpProgress_
  
> [in] Указатель на объект прогресса, отображает индикатор прогресса или NULL. Если _lpProgress_ является NULL, индикатор прогресса должен отображаться с помощью объекта progress, предоставленного MAPI с помощью [метода IMAPISupport::D oProgressDialog.](imapisupport-doprogressdialog.md) Параметр  _lpProgress_ игнорируется, если флаг AB_NO_DIALOG установлен в  _ulFlags_.
    
 _ulFlags_
  
> [in] Битмаска флагов, которые контролируют, как выполняется операция копирования. Можно установить следующие флаги:
    
AB_NO_DIALOG 
  
> Подавляет отображение индикатора прогресса. Если этот флаг не установлен, отображается индикатор прогресса.
    
CREATE_CHECK_DUP_LOOSE 
  
> Указывает на то, что должен быть выполнен свободный уровень проверки дублирующихся записей. Реализация свободной проверки дубликатов записей — это конкретный поставщик. Например, поставщик может определить свободный совпадение как любые две записи с одинаковым именем отображения.
    
CREATE_CHECK_DUP_STRICT 
  
> Указывает на то, что должен быть выполнен строгий уровень проверки записи дублирующихся записей. Реализация строгой проверки дубликатов записи является конкретным поставщиком. Например, поставщик может определить строгое соответствие как любые две записи с одинаковым именем отображения и адресом обмена сообщениями.
    
CREATE_REPLACE 
  
> Указывает, что новая запись должна заменить существующую, если установлено, что эти две записи являются дубликатами.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Операция копирования прошла успешно.
    
MAPI_W_PARTIAL_COMPLETION 
  
> Операция копирования в целом прошла успешно, но одну или несколько записей не удалось скопировать. Когда это значение возвращается, вызов должен быть обработан как успешный. Чтобы проверить это значение, используйте **HR_FAILED** макрос. Дополнительные сведения см. в [дополнительных сведениях Об использовании макроса для обработки ошибок.](using-macros-for-error-handling.md)
    
## <a name="remarks"></a>Примечания

Метод **IABContainer::CopyEntries** копирует записи из одного контейнера или другого контейнера. Вызов в **CopyEntries функционально** эквивалентен следующим вызовам для копирования каждой записи: 
  
1. Метод [IABContainer::CreateEntry](iabcontainer-createentry.md) для создания новой записи. 
    
2. Метод [IMAPIProp::GetProps](imapiprop-getprops.md) для чтения свойств из записи, которая будет скопирована. 
    
3. Метод [IMAPIProp::SetProps](imapiprop-setprops.md) для записи свойств в новую запись. 
    
4. Метод [IMAPIProp::SaveChanges](imapiprop-savechanges.md) новой записи для выполнения сохранения. 
    
5. Метод [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28VS.85%29.aspx) новой записи для выпуска ссылки контейнера. 
    
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Все контейнеры, поддерживают **метод IABContainer::CopyEntries,** должны быть модификабельными. Установите флаг AB_MODIFIABLE контейнера в **свойстве PR_CONTAINER_FLAGS** [(PidTagContainerFlags),](pidtagcontainerflags-canonical-property.md)чтобы указать, что он является модификационным. 
  
Необходимо поддерживать все флаги; однако интерпретация и использование этих флагов специфична для реализации, то есть можно определить, что означают семантика флагов CREATE_CHECK_DUP_LOOSE и CREATE_CHECK_DUP_STRICT в контексте реализации. Если вы не можете или не можете определить, является ли запись дублирующей, всегда разрешайте ее копирование. 
  
Если флаг CREATE_REPLACE, всегда копируйте запись независимо от CREATE_CHECK_DUP_LOOSE или CREATE_CHECK_DUP_STRICT и является ли запись дубликатом. 
  
Если CREATE_REPLACE не установлена и CREATE_CHECK_DUP_STRICT установлена, проверьте, есть ли дубликаты. Если запись определена как дубликат, не копируйте запись. 
  
Вам не нужно поддерживать CREATE_REPLACE; не поддержка CREATE_REPLACE означает, что вы можете безопасно игнорировать его и всегда выполнять копию. 
  
Возврат предупреждения MAPI_W_PARTIAL_COMPLETION только в том случае, если недюпликированная запись не может быть скопирована. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Используйте флаги CREATE_CHECK_DUP_LOOSE и CREATE_CHECK_DUP_STRICT, чтобы указать поставщику, как вы хотите, чтобы контейнер выполнял проверку дубликатов записи. Если необходимо добавить запись независимо от того, является ли она дубликатом, либо не установите ни один из этих флагов, ни CREATE_REPLACE флага. CREATE_REPLACE указывает, что вам не важно, является ли запись дубликатом; вы всегда хотите, чтобы она заменила исходную запись. 
  
## <a name="see-also"></a>См. также



[ENTRYLIST](entrylist.md)
  
[IABContainer::CreateEntry](iabcontainer-createentry.md)
  
[IMAPIProgress : IUnknown](imapiprogressiunknown.md)
  
[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[IABContainer : IMAPIContainer](iabcontainerimapicontainer.md)

