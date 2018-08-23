---
title: IMAPISupportDoCopyProps
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.DoCopyProps
api_type:
- COM
ms.assetid: 2446ef52-578a-4004-9719-de9b0207ccad
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: a30a323874c847d9a08b00512cfd30ff3cf5c5ff
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591130"
---
# <a name="imapisupportdocopyprops"></a>IMAPISupport::DoCopyProps

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Копирование или Перемещение одного или нескольких свойств объекта на другой объект.
  
```cpp
HRESULT DoCopyProps(
  LPCIID lpSrcInterface,
  LPVOID lpSrcObj,
  LPSPropTagArray lpIncludeProps,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  LPCIID lpDestInterface,
  LPVOID lpDestObj,
  ULONG ulFlags,
  LPSPropProblemArray FAR * lppProblems
);
```

## <a name="parameters"></a>Параметры

 _lpSrcInterface_
  
> [in] Указатель на идентификатор интерфейса (ИД интерфейса), который представляет интерфейс, который будет использоваться для доступа к объекту с помощью свойства, которые нужно скопировать или переместить.
    
 _lpSrcObj_
  
> [in] Указатель на объект, содержащий свойства, которые нужно скопировать или переместить.
    
 _lpIncludeProps_
  
> [in] Указатель на структуру [SPropTagArray](sproptagarray.md) , содержащий инвентаризации массив тегов свойств, которые указывают свойства, которые нужно скопировать или переместить. Параметр _lpIncludeProps_ не может быть NULL. 
    
 _ulUIParam_
  
> [in] Дескриптор родительского окна индикатор хода выполнения.
    
 _lpProgress_
  
> [in] Указатель на реализацию индикатор хода выполнения. Если значение NULL передается в параметре _lpProgress_ , с помощью реализации интерфейса MAPI отображается индикатор хода выполнения. Параметр _lpProgress_ игнорируется, пока флаг MAPI_DIALOG будет выполнен с помощью параметра _ulFlags_ . 
    
 _lpDestInterface_
  
> [in] Указатель на идентификатор интерфейса, который представляет интерфейс, который будет использоваться для доступа к объекту для получения свойства, которые копируются или перемещаются.
    
 _lpDestObj_
  
> [in] Указатель на объект для получения свойств копируемые или перемещения.
    
 _ulFlags_
  
> [in] Битовая маска флаги, который определяет, как выполняется операция копирования или перемещения. Можно задать следующие флажки:
    
MAPI_DIALOG 
  
> Отображает индикатор хода выполнения.
    
MAPI_MOVE 
  
> **DoCopyProps** следует выполнять операции перемещения вместо операцию копирования. Если этот флаг не задан, **DoCopyProps** выполняет операцию копирования. 
    
MAPI_NOREPLACE 
  
> Не следует перезаписывать существующие свойства в целевой объект. Если этот флаг не задан, **DoCopyProps** перезаписывает существующие свойства. 
    
 _lppProblems_
  
> [in, out] На входе указатель указатель на структуру [SPropProblemArray](spropproblemarray.md) ; в противном случае — значение NULL, указывает, не требуется выполнять сведения об ошибке. Если _lppProblems_ допустимый указатель на входные данные, **DoCopyProps** возвращает подробные сведения об ошибках в копирование одного или нескольких свойств. 
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> Свойства были успешно скопировать или переместить.
    
MAPI_E_COLLISION 
  
> Свойство так, чтобы скопировать или переместить уже существует в целевой объект и флаг MAPI_NOREPLACE. 
    
MAPI_E_FOLDER_CYCLE 
  
> Исходный объект прямо или косвенно содержит целевой объект. Важные может быть выполнено перед был обнаружен это условие, поэтому исходный и целевой объекты частично могут быть изменены. 
    
MAPI_E_INTERFACE_NOT_SUPPORTED 
  
> Интерфейс, определенного параметром _lpSrcInterface_ не поддерживается объектом источника или интерфейса, определенного параметром _lpDestInterface_ не поддерживается в целевой объект. 
    
MAPI_E_NO_ACCESS 
  
> Предпринята попытка получить доступ к объекту, для которого вызывающий не имеет разрешений. Эта ошибка возвращается в том случае, если в целевой объект совпадает с исходным объектом.
    
Возможные значения могут быть возвращены в структуре **SPropProblemArray** , но не как возвращаемые значения для **DoCopyProps**. Эти ошибки относятся к одному свойству.
  
MAPI_E_BAD_CHARWIDTH 
  
> Либо был установлен флажок MAPI_UNICODE и **DoCopyProps** не поддерживает Юникод, или MAPI_UNICODE не было установлено и **DoCopyProps** поддерживает только Юникод. 
    
MAPI_E_COMPUTED 
  
> Невозможно изменить свойство вызывающим абонентом, так как он является свойством только для чтения, вычисленный владельцем конечного объекта. Эта ошибка не является очень неблагоприятных; вызывающего абонента, должна поддерживать операции копирования для продолжения.
    
MAPI_E_INVALID_TYPE 
  
> Недопустимый тип свойства.
    
MAPI_E_UNEXPECTED_TYPE 
  
> Тип свойства не является типом, требующей вызывающего абонента.
    
## <a name="remarks"></a>Замечания

Метод **IMAPISupport::DoCopyProps** реализуется для объектов поддержки поставщика хранилища сообщений. Поставщики хранилища сообщений можно вызвать **DoCopyProps** , чтобы реализовать метод [IMAPIProp::CopyProps](imapiprop-copyprops.md) для своих папок и сообщений. **DoCopyProps** копирование или перемещение свойств, который определяются в массиве тег свойства, на который указывает _lpIncludeProps_ , и, представленные в объект, на который указывает _lpSrcObj_. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

При копировании свойств между объектами одного типа, таких как два сообщения параметры _lpSrcInterface_ и _lpDestInterface_ должен содержать те же интерфейс идентификатор и _lpSrcObj_ и _lpDestObj_ параметров должен указывать на объекты одного типа. Если _lpDestInterface_ имеет значение NULL, **DoCopyProps** возвращает MAPI_E_INVALID_PARAMETER. Если значение _lpDestInterface_ идентификатор приемлемой интерфейса, но набор _lpDestObj_ недопустимый указатель результаты непредсказуемы. Вероятнее всего поставщика завершится с ошибкой. 
  
Установите для флага MAPI_NOREPLACE не любое из свойств в целевой объект, требуется перезаписать. Свойства в целевом объекте, существующих в исходном объекте и не перезаписываются не удалить или изменить.
  
Чтобы скопировать список получателей сообщения, включите свойство **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) в массиве тег свойство указывает параметр _lpIncludeProps_ . Чтобы скопировать вложений сообщений, включите свойство **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)). 
  
Чтобы скопировать папку или иерархии контейнер адресной книги или таблицу содержимого, включают **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) или **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) в массиве тега свойства. Чтобы включить таблицу связанного содержимого папки, добавьте свойство **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) в массиве.
  
Если вложенные папки копирования или перемещения, их содержимое перемещаются или копируются полностью, независимо от того, использование свойств, указанный в параметре **SPropTagArray** структуры. 
  
 **DoCopyProps** отчетов глобального ошибки, возникающие при работе с операции в целом и отдельных ошибки, возникающие при работе с одного или нескольких свойств. Эти отдельные ошибки помещаются в структуре **SPropProblemArray** . Отчеты на уровне свойств, передав значение NULL, а не является допустимым указателем, для параметра свойство массива проблема структура об ошибках, можно отключить. 
  
Если вы хотите получать сведения об ошибках, передайте допустимый указатель структура **SPropProblemArray** с помощью параметра _lppProblems_ . При **DoCopyProps** возвращает значение S_OK, проверьте наличие возможных ошибок с помощью отдельных свойств в структуре. Когда **DoCopyProps** возвращает ошибку, не информация возвращается в структуре **SPropProblemArray** . Вместо этого вызовите метод [IMAPISupport::GetLastError](imapisupport-getlasterror.md) , чтобы получить подробные сведения об ошибке. 
  
Если **DoCopyProps** возвращает значение S_OK, освободите возвращенные структура **SPropProblemArray** путем вызова функции [MAPIFreeBuffer](mapifreebuffer.md) . 
  
## <a name="see-also"></a>См. также



[IMAPIProp::CopyProps](imapiprop-copyprops.md)
  
[IMAPISupport::CopyMessages](imapisupport-copymessages.md)
  
[IMAPISupport::DoCopyTo](imapisupport-docopyto.md)
  
[IMAPISupport::GetLastError](imapisupport-getlasterror.md)
  
[Каноническое свойство PidTagContainerContents](pidtagcontainercontents-canonical-property.md)
  
[Каноническое свойство PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)
  
[Каноническое свойство PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)
  
[Каноническое свойство PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)
  
[Каноническое свойство PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)
  
[SPropProblemArray](spropproblemarray.md)
  
[SPropTagArray](sproptagarray.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

