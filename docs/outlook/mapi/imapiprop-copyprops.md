---
title: IMAPIPropCopyProps
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProp.CopyProps
api_type:
- COM
ms.assetid: f65da1c8-d49b-44e8-8c66-9c53d088d334
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 7319f1abb4a74ee17b0a4a1220215c29434d256b
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25398404"
---
# <a name="imapipropcopyprops"></a>IMAPIProp::CopyProps

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Копирование или Перемещение выбранных свойств. 
  
```cpp
HRESULT CopyProps(
  LPSPropTagArray lpIncludeProps,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  LPCIID lpInterface,
  LPVOID lpDestObj,
  ULONG ulFlags,
  LPSPropProblemArray FAR * lppProblems
);
```

## <a name="parameters"></a>Параметры

 _lpIncludeProps_
  
> [in] Указатель в массив тега свойства, который задает свойства, которые нужно скопировать или переместить. **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) нельзя включить в массиве. Параметр _lpIncludeProps_ не может быть **null**.
    
 _ulUIParam_
  
> [in] Дескриптор родительского окна индикатор хода выполнения. 
    
 _lpProgress_
  
> [in] Указатель на реализацию индикатор хода выполнения. Если **значение null,** передается в параметре _lpProgress_ , с помощью реализации интерфейса MAPI отображается индикатор хода выполнения. Параметр _lpProgress_ игнорируется, пока флаг MAPI_DIALOG будет выполнен с помощью параметра _ulFlags_ . 
    
 _lpInterface_
  
> [in] Указатель на идентификатор интерфейса (ИД интерфейса), который представляет интерфейс, который должен использоваться для доступа к объекту, на который указывает параметр _lpDestObj_ . Параметр _lpInterface_ не должно быть **значение null**.
    
 _lpDestObj_
  
> [in] Указатель на объект для получения свойств копируемые или перемещения.
    
 _ulFlags_
  
> [in] Битовая маска флаги, который определяет операцию копирования или перемещения. Можно задать следующие флажки:
    
MAPI_DECLINE_OK 
  
> Если **CopyProps** вызывает метод [IMAPISupport::DoCopyProps](imapisupport-docopyprops.md) для обработки копировать или перемещать операции, она немедленно вместо этого возвращает со значением ошибки MAPI_E_DECLINE_COPY. Флаг MAPI_DECLINE_OK задается MAPI для ограничения рекурсии. Клиенты не задан этот флаг. 
    
MAPI_DIALOG 
  
> Отображает индикатор хода выполнения.
    
MAPI_MOVE 
  
> **CopyProps** следует выполнять операции перемещения вместо операцию копирования. Если этот флаг не задан, **CopyProps** выполняет операцию копирования. 
    
MAPI_NOREPLACE 
  
> Не следует перезаписывать существующие свойства в целевой объект. Если этот флаг не задан, **CopyProps** перезаписывает существующие свойства. 
    
 _lppProblems_
  
> [in, out] На входе указатель указатель на структуру [SPropProblemArray](spropproblemarray.md) ; в противном случае — **значение null**, указывающего на то, что нет необходимости для получения сведений об ошибках. Если _lppProblems_ допустимый указатель на входные данные, **CopyProps** возвращает подробные сведения об ошибках в копирование одного или нескольких свойств. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Свойства успешно копирования или перемещения.
    
MAPI_E_COLLISION 
  
> Не удается скопировать вложенные объекты, так как вложенные объекты с одинаковыми именами display, определенные в свойстве **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) уже существует в целевой объект. 
    
MAPI_E_DECLINE_COPY 
  
> Поставщик услуг не реализует операцию копирования.
    
MAPI_E_FOLDER_CYCLE 
  
> Исходный объект для выполнения операции копирования или перемещения прямо или косвенно содержит целевой объект. Важные может быть выполнено перед был обнаружен это условие, поэтому исходный и целевой объекты частично могут быть изменены. 
    
MAPI_E_INTERFACE_NOT_SUPPORTED 
  
> Интерфейс, определенного параметром _lpInterface_ не поддерживается в целевой объект. 
    
MAPI_E_NO_ACCESS 
  
> Предпринята попытка получить доступ к объекту, для которого вызывающий не имеет разрешений. Эта ошибка возвращается в том случае, если в целевой объект совпадает с исходным объектом.
    
Возможные значения могут быть возвращены в структуре **SPropProblemArray** , но не как возвращаемые значения для **CopyProps**. Эти ошибки относятся к одному свойству.
  
MAPI_E_BAD_CHARWIDTH 
  
> Либо был установлен флажок MAPI_UNICODE и **CopyProps** не поддерживает Юникод, или MAPI_UNICODE не было установлено и **CopyProps** поддерживает только Юникод. 
    
MAPI_E_COMPUTED 
  
> Невозможно изменить свойство вызывающим абонентом, так как он является свойством только для чтения, вычисленный владельцем конечного объекта. Эта ошибка не является очень неблагоприятных; вызывающего абонента, должна поддерживать операции копирования для продолжения.
    
MAPI_E_INVALID_TYPE 
  
> Недопустимый тип свойства.
    
MAPI_E_UNEXPECTED_TYPE 
  
> Тип свойства не типа, вызывающего абонента.
    
## <a name="remarks"></a>Примечания

Метод **IMAPIProp::CopyProps** копирует или перемещает выбранные свойства из текущего объекта в целевой объект. **CopyProps** используется в основном для ответа и пересылки сообщений, где только некоторые свойства из исходного сообщения организации, ответ или перенаправлять копии. 
  
Вложенными объектами в объекте источника автоматически включены в операции и перемещаются или копируются полностью, независимо от того, использование свойств, указанный в параметре [SPropTagArray](sproptagarray.md) структуры. По умолчанию **CopyProps** перезаписывает любые свойства в целевом объекте, соответствующие свойства из исходного объекта. Если какие-либо свойства скопированной или перемещенной уже существует в целевом объекте, существующие свойства перезаписываются новых свойств, пока флаг MAPI_NOREPLACE будет выполнен с помощью параметра _ulFlags_ . Существующие данные в целевой объект, который не перезаписывается остаются без изменений. 
  
## <a name="notes-to-implementers"></a>Примечания для реализующих

Можно предоставить полная реализация **CopyProps** или зависеть от реализации, предоставляющий MAPI в своем объекте поддержки. Если вы хотите использовать в реализации интерфейса MAPI, вызовите метод **IMAPISupport::DoCopyProps** . Если делегирование обработки для **DoCopyProps** и передаются флаг MAPI_DECLINE_OK, избежать вызова поддержки и вместо этого возвращать MAPI_E_DECLINE_COPY. Этот флаг вызываемого с MAPI, чтобы избежать возможных рекурсии, которая может возникнуть при копировании папки. 
  
Так как операция копирования может быть длинным, должны отображать индикатор хода выполнения. Описание использования реализации [IMAPIProgress](imapiprogressiunknown.md) , переданной в параметре _lpProgress_ , если он существует. Если _lpProgress_ имеет **значение null**, вызовите метод [IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md) для использования в реализации интерфейса MAPI. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Не задан флаг MAPI_DECLINE_OK; он используется MAPI при его вызове для сообщения **CopyProps** реализации поставщика хранилища. 
  
Так как операции копирования и перемещения может потребоваться времени, имеет смысл запросить отображение индикатор хода выполнения, установив флаг MAPI_DIALOG. Можно задать параметр _lpProgress_ для внедрения **IMAPIProgress**, если такой существует, или значение **null**. Если _lpProgress_ имеет **значение null**, **CopyProps** будет использовать индикатор хода выполнения по умолчанию, предоставленные MAPI. 
  
Можно отключить отображение индикатора хода выполнения, не задав флаг MAPI_DIALOG. **CopyProps** будет игнорировать параметры _ulUIParam_ и _lpProgress_ и избежать отображения индикатора. 
  
 **CopyProps** можно сообщить о глобальном уровне и на отдельные ошибки или ошибки, возникающие при работе с одного или нескольких свойств. Эти отдельные ошибки помещаются в структуре **SPropProblemArray** . Отчеты на уровне свойств, передав **значение null**, а не является допустимым указателем, для параметра свойство массива проблема структура об ошибках, можно отключить. 
  
Если вы хотите получать сведения об ошибках, передайте допустимый указатель структура **SPropProblemArray** с помощью параметра _lppProblems_ . При **CopyProps** возвращает значение S_OK, проверьте наличие возможных ошибок с помощью отдельных свойств в структуре. Когда **CopyProps** возвращает ошибку, не информация возвращается в структуре **SPropProblemArray** . Вместо этого вызовите метод [IMAPIProp::GetLastError](imapiprop-getlasterror.md) , чтобы получить подробные сведения об ошибке. 
  
Если **CopyProps** возвращает значение S_OK, освободите возвращенные структура **SPropProblemArray** путем вызова функции [MAPIFreeBuffer](mapifreebuffer.md) . 
  
При копировании свойств, которые являются уникальными для объекта тип источника данных, необходимо убедиться, что целевой объект является одного типа. **CopyProps** не запрещает связывания свойства, которые обычно относятся к один тип объекта, с другой тип объекта. Зависит от пользователя для копирования свойств, которые нужны для конечного объекта. К примеру не следует копировать свойства сообщений к контейнеру адресной книги. 
  
Чтобы убедиться, что выполняется копирование между объектами одного типа, убедитесь, что установлен исходный и конечный объект того же типа, путем сравнения указателей объектов или вызова метода [IUnknown::QueryInterface](https://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx) . Задайте идентификатор интерфейса, на который указывает _lpInterface_ стандартный интерфейс для объекта источника. Кроме того убедитесь, что тип объекта или свойство **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)) является общим для двух объектов. Например при копировании из сообщения значение _lpInterface_ IID_IMessage и **PR_OBJECT_TYPE** объекты MAPI_MESSAGE. 
  
Если недопустимый указатель передается в параметре _lpDestObj_ , результаты непредсказуемы. 
  
Чтобы скопировать список получателей сообщения, вызовите метод **CopyProps** сообщение и включите свойство **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) в массиве тега свойства. Чтобы скопировать вложений сообщений, включите свойство **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)). 
  
Для копирования папки или иерархии контейнер адресной книги или таблицу содержимого, включают **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) или свойств **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) Свойство tag массива. Чтобы включить таблицу связанного содержимого папки, добавьте свойство **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) в массиве. 
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|MAPIFunctions.cpp  <br/> |CopyNamedProps  <br/> |Mfcmapi (en) использует метод **IMAPIProp::CopyProps** для копирования одного сообщения именованных свойств.  <br/> |
|SingleMAPIPropListCtrl.cpp  <br/> |CSingleMAPIPropListCtrl::OnPasteProperty  <br/> |Mfcmapi (en) использует метод **IMAPIProp::CopyProps** для вставки свойства, скопированный из другого объекта.  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPIFolder::CopyMessages](imapifolder-copymessages.md)
  
[IMAPIProgress : IUnknown](imapiprogressiunknown.md)
  
[IMAPIProp::CopyTo](imapiprop-copyto.md)
  
[IMAPIProp::GetLastError](imapiprop-getlasterror.md)
  
[IMAPISupport::DoCopyProps](imapisupport-docopyprops.md)
  
[IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[Каноническое свойство PidTagContainerContents](pidtagcontainercontents-canonical-property.md)
  
[Каноническое свойство PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)
  
[Каноническое свойство PidTagDisplayName](pidtagdisplayname-canonical-property.md)
  
[Каноническое свойство PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)
  
[Каноническое свойство PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)
  
[Каноническое свойство PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)
  
[Каноническое свойство PidTagObjectType](pidtagobjecttype-canonical-property.md)
  
[SPropProblemArray](spropproblemarray.md)
  
[SPropTagArray](sproptagarray.md)
  
[IMAPIProp : IUnknown](imapipropiunknown.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

