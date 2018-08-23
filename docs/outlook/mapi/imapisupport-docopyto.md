---
title: IMAPISupportDoCopyTo
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.DoCopyTo
api_type:
- COM
ms.assetid: 84019475-5176-4fc5-a3ee-871095077498
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 5ce5aa8c43e284b493a0709808a196c6c6889f88
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592110"
---
# <a name="imapisupportdocopyto"></a>IMAPISupport::DoCopyTo

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Копирование или перемещение всех свойств одного объекта, за исключением специально исключенные свойства на другой объект.
  
```cpp
HRESULT DoCopyTo(
  LPCIID lpSrcInterface,
  LPVOID lpSrcObj,
  ULONG ciidExclude,
  LPCIID rgiidExclude,
  LPSPropTagArray lpExcludeProps,
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
  
> [in] Указатель на идентификатор интерфейса (ИД интерфейса), который представляет интерфейс, который будет использоваться для доступа к объекту, который имеет свойства, которые нужно скопировать или переместить.
    
 _lpSrcObj_
  
> [in] Указатель на объект, который содержит свойства, которые нужно скопировать или переместить.
    
 _ciidExclude_
  
> [in] Число интерфейсов следует исключить при скопируйте или переместите свойства.
    
 _rgiidExclude_
  
> [in] Массив идентификаторов интерфейса, которое указывает, интерфейсы, которые не должны использоваться при скопируйте или переместите дополнительную информацию в целевой объект.
    
 _lpExcludeProps_
  
> [in] Указатель в массив тег свойства, который определяет свойство теги, которые следует исключить из копии или операции перемещения. Указать значение NULL для параметра _lpExcludeProps_ указывает, что все свойства объекта следует скопировать или переместить. **DoCopyTo** возвращает MAPI_E_INVALID_PARAMETER при член **cValues** структуры [SPropTagArray](sproptagarray.md) указывает _lpExcludeProps_ имеет значение 0. 
    
 _ulUIParam_
  
> [in] Дескриптор родительского окна индикатор хода выполнения. 
    
 _lpProgress_
  
> [in] Указатель на реализацию индикатор хода выполнения. Если значение NULL передается в параметре _lpProgress_ , MAPI предоставляет реализацию хода выполнения. Параметр _lpProgress_ игнорируется, пока флаг MAPI_DIALOG будет выполнен с помощью параметра _ulFlags_ . 
    
 _lpDestInterface_
  
> [in] Указатель на интерфейс идентификатор, который представляет интерфейс, который будет использоваться для доступа к объекту для получения свойства копируемые или перемещения.
    
 _lpDestObj_
  
> [in] Указатель на объект для получения свойств копируемые или перемещения.
    
 _ulFlags_
  
> [in] Битовая маска флаги, который определяет операцию копирования или перемещения. Можно задать следующие флажки:
    
MAPI_DIALOG 
  
> Отображает индикатор хода выполнения. 
    
MAPI_MOVE 
  
> **DoCopyTo** следует выполнять операции перемещения вместо операцию копирования. Если этот флаг не задан, **DoCopyTo** выполняет операцию копирования. 
    
MAPI_NOREPLACE 
  
> Не следует перезаписывать существующие свойства в целевой объект. Если этот флаг не задан, **DoCopyTo** перезаписывает существующие свойства. 
    
 _lppProblems_
  
> [out] На входе указатель указатель на структуру [SPropProblemArray](spropproblemarray.md) ; в противном случае — значение NULL, указывает, не требуется выполнять сведения об ошибке. Если _lppProblems_ допустимый указатель на входные данные, **DoCopyTo** возвращает подробные сведения об ошибках в копирование одного или нескольких свойств. 
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> Свойства успешно копирования или перемещения.
    
MAPI_E_COLLISION 
  
> Свойство так, чтобы скопировать или переместить уже существует в целевой объект и флаг MAPI_NOREPLACE. 
    
MAPI_E_FOLDER_CYCLE 
  
> Исходный объект прямо или косвенно содержит целевой объект. Важные может быть выполнено перед был обнаружен это условие, поэтому исходный и целевой объекты частично могут быть изменены. 
    
MAPI_E_INTERFACE_NOT_SUPPORTED 
  
> Интерфейс, определенного параметром _lpSrcInterface_ не поддерживается объектом, на который указывает _lpSrcObj_или интерфейса, определенного параметром _lpDestInterface_ не поддерживается объектом, на который указывает _lpDestObj _. 
    
MAPI_E_NO_ACCESS 
  
> Предпринята попытка получить доступ к объекту, для которого вызывающий не имеет разрешений. Эта ошибка возвращается в том случае, если в целевой объект совпадает с исходным объектом.
    
MAPI_E_INVALID_PARAMETER 
  
> Параметр _lpSrcInterface_ имеет значение NULL. 
    
Возможные значения могут быть возвращены в структуре **SPropProblemArray** , но не как возвращаемые значения для **DoCopyTo**. Эти ошибки относятся к одному свойству.
  
MAPI_E_BAD_CHARWIDTH 
  
> Либо был установлен флажок MAPI_UNICODE и **DoCopyTo** не поддерживает Юникод, или MAPI_UNICODE не было установлено и **DoCopyTo** поддерживает только Юникод. 
    
MAPI_E_COMPUTED 
  
> Невозможно изменить свойство вызывающим абонентом, так как он является свойством только для чтения, вычисленный владельцем конечного объекта. Эта ошибка не является очень неблагоприятных; вызывающего абонента, должна поддерживать операции копирования для продолжения.
    
MAPI_E_INVALID_TYPE 
  
> Недопустимый тип свойства.
    
MAPI_E_UNEXPECTED_TYPE 
  
> Тип свойства не типа, вызывающего абонента.
    
## <a name="remarks"></a>Замечания

Метод **IMAPISupport::DoCopyTo** реализуется для объектов поддержки поставщика хранилища сообщений. Поставщики хранилища сообщений можно вызвать **DoCopyTo** , чтобы реализовать метод [IMAPIProp::CopyTo](imapiprop-copyto.md) для своих папок и сообщений. 
  
По умолчанию **DoCopyTo** копирует или переносит все свойства одного объекта на другой объект. Вложенными объектами в объекте источника автоматически включены в операции и скопировать или переместить полностью. 
  
Если какие-либо свойства скопированной или перемещенной уже существует в целевом объекте, существующие свойства перезаписываются новых свойств, пока флаг MAPI_NOREPLACE будет выполнен с помощью параметра _ulFlags_ . Существующие данные в целевой объект, который не перезаписывается остаются без изменений. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Чтобы исключить свойства из копии или операции перемещения, включают теги их свойства с помощью параметра _lpExcludeProps_ . При передаче результатов с помощью макроса [PROP_TAG](prop_tag.md) для построения тега свойства из указанный идентификатор в массиве тега свойства будут исключены все свойства с этим идентификатором. Например следующую запись в массиве тега свойства вызывает все свойства с идентификатором 0x8002, чтобы исключить, независимо от типа: 
  
 `PROP_TAG(PT_LONG, 0x8002)`
  
Чтобы предотвратить копирование время доставки сообщений, при копировании сообщения в другую папку, укажите **PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)) в массиве свойство tag исключить. Чтобы исключить список получателей сообщения, добавьте свойство **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) в массиве исключить. Чтобы исключить вложений сообщений, добавьте свойство **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) в массиве.
  
Аналогичным образом чтобы предотвратить копирование или перемещение папки или иерархии контейнер адресной книги или таблицу содержимого, включите **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) или **PR_CONTAINER_CONTENTS** ([ PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) в свойстве тег исключить массива.
  
Пропуск MAPI_E_COMPUTED ошибок, возвращаемых в структуре **SPropProblemArray** в параметре _lppProblems_ . 
  
Идентификатор, который _lpSrcInterface_ моменты, которые обычно является то же, что идентификатор интерфейса, указывающего _lpDestInterface_ . 
  
Если передать идентификатор приемлемой интерфейса в _lpDestInterface_ , но недопустимый указатель в _lpDestObj_результаты непредсказуемы. Вероятнее всего это приведет к поставщику могут быть. 
  
С другой стороны Если принять во внимание дополнительную информацию, которая не должна быть скопированы или перемещены, добавьте идентификаторы интерфейса для интерфейсов исключить в массиве, переданной в параметре _rgiidExclude_ . Например при копировании сообщения, но не какие-либо из их вложений сообщений передайте IID_IMessage в массиве _rgiidExclude_ . **DoCopyTo** игнорирует любые интерфейсов, перечисленных в _rgiidExclude_ , который не распознается. 
  
Если используется параметр _rgiidExclude_ следует исключить интерфейс также исключаются все интерфейсы, производные от этого интерфейса. К примеру за исключением интерфейса [IMAPIContainer](imapicontainerimapiprop.md) включен, папки или контейнеров адресной книги для исключения, в зависимости от типа поставщика. Не исключить [IMAPIProp](imapipropiunknown.md) или [IUnknown](http://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) из-за слишком большом числе интерфейсы производные от них. 
  
 **DoCopyTo** отчетов глобальной ошибки, которые применяются к операции в целом и отдельных ошибок, которые применяются для отдельных свойств. Эти отдельные ошибки помещаются в структуре **SPropProblemArray** . Отчеты на уровне свойств, передав значение NULL, а не является допустимым указателем, для параметра свойство массива проблема структура об ошибках, можно отключить. 
  
Если вы хотите получать сведения об ошибках, передайте допустимый указатель структура **SPropProblemArray** с помощью параметра _lppProblems_ . При **DoCopyTo** возвращает значение S_OK, проверьте наличие возможных ошибок с помощью отдельных свойств в структуре. Когда **DoCopyTo** возвращает ошибку, не информация возвращается в структуре **SPropProblemArray** . Вместо этого вызовите метод [IMAPISupport::GetLastError](imapisupport-getlasterror.md) , чтобы получить подробные сведения об ошибке. 
  
Если **DoCopyTo** возвращает значение S_OK, освободите возвращенные структура **SPropProblemArray** путем вызова функции [MAPIFreeBuffer](mapifreebuffer.md) . 
  
Если глобальные ошибка возникает при вызове **DoCopyTo** , не используйте или Бесплатная загрузка структуры **SPropProblemArray** . Поставщики следует игнорировать член _ulIndex_ в **SPropProblemArray** структуры, возвращаемые **DoCopyTo**.
  
## <a name="see-also"></a>См. также



[IMAPIProp::CopyTo](imapiprop-copyto.md)
  
[IMAPISupport::CopyFolder](imapisupport-copyfolder.md)
  
[IMAPISupport::CopyMessages](imapisupport-copymessages.md)
  
[IMAPISupport::GetLastError](imapisupport-getlasterror.md)
  
[Каноническое свойство PidTagContainerContents](pidtagcontainercontents-canonical-property.md)
  
[Каноническое свойство PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)
  
[Каноническое свойство PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)
  
[Каноническое свойство PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)
  
[Каноническое свойство PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)
  
[SPropProblemArray](spropproblemarray.md)
  
[SPropTagArray](sproptagarray.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

