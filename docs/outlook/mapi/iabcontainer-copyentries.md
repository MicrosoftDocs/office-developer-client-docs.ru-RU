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
ms.openlocfilehash: 44a31e46c43a065c720564f2aa193913dbfd9a2e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808704"
---
# <a name="iabcontainercopyentries"></a>IABContainer::CopyEntries

  
  
**Относится к**: Outlook 
  
Копирует один или несколько операций, пользователи обычно обмена мгновенными сообщениями или списки рассылки.
  
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
  
> [in] Указатель на массив структур [ENTRYLIST](entrylist.md) , который содержит идентификаторы записей записей для копирования. 
    
 _ulUIParam_
  
> [in] Дескриптор родительского окна все диалоговые окна или окна, которые отображаются этот метод. Параметр _ulUIParam_ должно быть равно нулю, если флаг AB_NO_DIALOG установлен в параметре _ulFlags_ . 
    
 _lpProgress_
  
> [in] Указатель на объект хода выполнения, который отображает индикатор выполнения или значение NULL. Если _lpProgress_ имеет значение NULL, с помощью объекта ход выполнения, предоставляемые MAPI через метод [IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md) должно отображаться индикатор хода выполнения. Параметр _lpProgress_ игнорируется, если флаг AB_NO_DIALOG установлен в _ulFlags_.
    
 _ulFlags_
  
> [in] Битовая маска флаги, который определяет, как выполняется операция копирования. Можно задать следующие флажки:
    
AB_NO_DIALOG 
  
> Запрещает отображение индикатора хода выполнения. Если этот флаг не установлен, отображается индикатор хода выполнения.
    
CREATE_CHECK_DUP_LOOSE 
  
> Указывает, что свободный уровень проверки повторяющихся запись должна быть выполнена. Реализация проверки свободном дубликат зависит от поставщика. Например поставщик можно определить неточное соответствие две записи, с одинаковым отображаемое имя.
    
CREATE_CHECK_DUP_STRICT 
  
> Указывает, что strict уровень проверки повторяющихся запись должна быть выполнена. Реализация strict дубликат проверки зависит от поставщика. Например поставщик можно определить строгое соответствие две записи, оба с одинаковым отображать имя и адрес для сообщений.
    
CREATE_REPLACE 
  
> Указывает, что новая запись необходимо заменить существующий, если определено, что они дубликатов.
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> Операция копирования выполнена успешно.
    
MAPI_W_PARTIAL_COMPLETION 
  
> Операции копирования в целом прошло успешно, но не удалось скопировать один или несколько записей. При возвращении это значение вызова необходимо обрабатывать об успешном завершении. Чтобы проверить это значение, используйте макрос **HR_FAILED** . Дополнительные сведения можно [С помощью макросов для обработки ошибок](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Замечания

Метод **IABContainer::CopyEntries** копирует записи из другой контейнер или же контейнера. Вызов **CopyEntries** функционально эквивалентна выполнение следующих вызовов для каждой записи для копирования: 
  
1. Метод [IABContainer::CreateEntry](iabcontainer-createentry.md) , чтобы создать новую запись. 
    
2. Метод [IMAPIProp::GetProps](imapiprop-getprops.md) для чтения свойства из записи, которую требуется скопировать. 
    
3. Метод [IMAPIProp::SetProps](imapiprop-setprops.md) для записи свойств в новую запись. 
    
4. Метод [IMAPIProp::SaveChanges](imapiprop-savechanges.md) новую запись для выполнения сохранения. 
    
5. Метод [функции IUnknown::Release](http://msdn.microsoft.com/en-us/library/ms682317%28VS.85%29.aspx) новую запись для освобождения ссылку контейнера. 
    
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Все контейнеры, поддерживающие метод **IABContainer::CopyEntries** значения можно изменить. Установите флаг AB_MODIFIABLE контейнера в своем свойстве **PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)), чтобы указать, что он или нет. 
  
Должна поддерживать все флажки; Тем не менее, интерпретации и использовании этих флагов зависит от реализации, то есть, вы можете определить означает в контексте внедрения семантика флаги CREATE_CHECK_DUP_LOOSE и CREATE_CHECK_DUP_STRICT. Если не удается или не определить, является ли запись дубликата всегда разрешать записи, которую требуется скопировать. 
  
Если флаг CREATE_REPLACE имеет значение, всегда копировать записи вне зависимости от ли CREATE_CHECK_DUP_LOOSE или CREATE_CHECK_DUP_STRICT устанавливается и ли операция совпадает со значением. 
  
Если CREATE_CHECK_DUP_STRICT имеет значение CREATE_REPLACE не установлена, проверьте наличие дубликатов. Если запись определяется дубликатом, не копируйте записи. 
  
Необходимо поддерживать CREATE_REPLACE; не поддерживает CREATE_REPLACE означает, что можно проигнорировать и всегда выполнить копирование. 
  
Возвращает предупреждение MAPI_W_PARTIAL_COMPLETION только в том случае, если не удается скопировать неповторяющихся запись. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Используйте флаги CREATE_CHECK_DUP_LOOSE и CREATE_CHECK_DUP_STRICT для указания к поставщику того, как контейнер для выполнения проверки повторяющихся запись. Если вам потребуется добавлена независимо от того, будет ли это дублировать записи, не задавайте для этих флагов или установить флаг CREATE_REPLACE. CREATE_REPLACE указывает, что не нужно, если запись уже существует; всегда необходимо заменить исходной записи. 
  
## <a name="see-also"></a>См. также



[ENTRYLIST](entrylist.md)
  
[IABContainer::CreateEntry](iabcontainer-createentry.md)
  
[IMAPIProgress : IUnknown](imapiprogressiunknown.md)
  
[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[IABContainer : IMAPIContainer](iabcontainerimapicontainer.md)

