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
ms.openlocfilehash: 6f6c802f1d5ead1750c05fafc54533487fe3732a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331810"
---
# <a name="imapisupportdocopyto"></a>IMAPISupport::DoCopyTo

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Копирует или перемещает все свойства одного объекта, за исключением специально исключенных свойств, в другой объект.
  
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

## <a name="parameters"></a>Parameters

 _lpSrcInterface_
  
> [in] Указатель на идентификатор интерфейса (IID), который представляет интерфейс, который будет использоваться для доступа к объекту, который имеет свойства, которые необходимо скопировать или перена перемещать.
    
 _lpSrcObj_
  
> [in] Указатель на объект, у него есть свойства, которые необходимо скопировать или перена перемещать.
    
 _ciidExclude_
  
> [in] Количество интерфейсов, которые необходимо исключить при копировании или перемещения свойств.
    
 _rgiidExclude_
  
> [in] Массив идентификаторов интерфейса, который указывает интерфейсы, которые не следует использовать при копировании или перемещение дополнительных сведений в объект назначения.
    
 _lpExcludeProps_
  
> [in] Указатель на массив тегов свойств, который определяет теги свойств, которые следует исключить из операции копирования или перемещения. Передача NULL в  _параметре lpExcludeProps_ указывает на то, что все свойства объекта должны быть скопированы или перемещены. **DoCopyTo** возвращает MAPI_E_INVALID_PARAMETER, когда член **cValues** структуры [SPropTagArray,](sproptagarray.md) на который указывает  _lpExcludeProps,_ задает 0. 
    
 _ulUIParam_
  
> [in] Ручка родительского окна индикатора прогресса. 
    
 _lpProgress_
  
> [in] Указатель на реализацию индикатора прогресса. Если NULL передается в  _параметре lpProgress,_ MAPI обеспечивает реализацию прогресса. Параметр _lpProgress_ игнорируется, если флаг MAPI_DIALOG в параметре _ulFlags._ 
    
 _lpDestInterface_
  
> [in] Указатель на идентификатор интерфейса, который представляет интерфейс, который будет использоваться для доступа к объекту для получения скопированные или перенесенные свойства.
    
 _lpDestObj_
  
> [in] Указатель на объект для получения скопированные или перенесенные свойства.
    
 _ulFlags_
  
> [in] Битмашка флагов, которые контролируют операцию копирования или перемещения. Можно установить следующие флаги:
    
MAPI_DIALOG 
  
> Отображает индикатор прогресса. 
    
MAPI_MOVE 
  
> **DoCopyTo** должен выполнять операцию перемещения вместо операции копирования. Если этот флаг не установлен, **DoCopyTo** выполняет операцию копирования. 
    
MAPI_NOREPLACE 
  
> Существующие свойства в объекте назначения не должны быть перезаписаны. Если этот флаг не установлен, **DoCopyTo** переописает существующие свойства. 
    
 _lppProblems_
  
> [вышел] На входе указатель на указатель на [структуру SPropProblemArray;](spropproblemarray.md) в противном случае NULL, что не указывает на отсутствие необходимости в сведениях об ошибках. Если  _lppProblems_ является допустимым указателем на входе, **DoCopyTo** возвращает подробные сведения об ошибках при копировании одного или более свойств. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Свойства были успешно скопированы или перемещены.
    
MAPI_E_COLLISION 
  
> Свойство, которое будет скопировано или перемещено, уже существует в объекте назначения, MAPI_NOREPLACE задает флаг. 
    
MAPI_E_FOLDER_CYCLE 
  
> Исходный объект прямо или косвенно содержит объект назначения. Перед обнаружением этого условия, возможно, была выполнена значительная работа, поэтому объекты источника и назначения могут быть частично изменены. 
    
MAPI_E_INTERFACE_NOT_SUPPORTED 
  
> Интерфейс, идентифицированный параметром  _lpSrcInterface,_ не поддерживается объектом, на который указывает  _lpSrcObj,_ или интерфейс, идентифицированный параметром  _lpDestInterface,_ не поддерживается объектом, на который указывает  _lpDestObj_. 
    
MAPI_E_NO_ACCESS 
  
> Была предпринята попытка доступа к объекту, для которого у вызываемого недостаточно разрешений. Эта ошибка возвращается, если объект назначения является таким же, как и исходный объект.
    
MAPI_E_INVALID_PARAMETER 
  
> Параметр  _lpSrcInterface_ — NULL. 
    
Следующие значения могут быть возвращены в **структуре SPropProblemArray,** но не в качестве значений возврата **для DoCopyTo.** Эти ошибки применимы к одному свойству.
  
MAPI_E_BAD_CHARWIDTH 
  
> Либо флаг MAPI_UNICODE был установлен, а **DoCopyTo** не поддерживает Юникод, либо MAPI_UNICODE не задавалось, а **DoCopyTo** поддерживает только Юникод. 
    
MAPI_E_COMPUTED 
  
> Свойство не может быть изменено вызываемой, так как оно является свойством только для чтения, вычисляется владельцем объекта назначения. Эта ошибка не является серьезной; вызываемая должна разрешить продолжение операции копирования.
    
MAPI_E_INVALID_TYPE 
  
> Тип свойства недействителен.
    
MAPI_E_UNEXPECTED_TYPE 
  
> Тип свойства не является типом, ожидаемым вызываемой.
    
## <a name="remarks"></a>Примечания

Метод **IMAPISupport::D oCopyTo** реализован для объектов поддержки поставщиков сообщений. Поставщики магазинов сообщений могут вызвать **DoCopyTo** для реализации метода [IMAPIProp::CopyTo](imapiprop-copyto.md) для своих папок и сообщений. 
  
По умолчанию **DoCopyTo** копирует или перемещает все свойства одного объекта на другой объект. Любые подобъекты в объекте источника автоматически включаются в операцию и копируются или перемещаются в полном объеме. 
  
Если какие-либо из скопированные или перемещенные свойства уже существуют в объекте назначения, существующие свойства перезаписываются новыми свойствами, если флаг MAPI_NOREPLACE не задан в параметре _ulFlags._ Существующая информация в объекте назначения, который не перезаписан, остается нетронутой. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Чтобы исключить свойства из операции копирования или перемещения, включи их теги свойств в параметр _lpExcludeProps._ Если вы передаете результаты использования [макроса PROP_TAG](prop_tag.md) для создания тега свойств из определенного идентификатора в массиве тегов свойств, все свойства с этим идентификатором будут исключены. Например, следующая запись в массиве тегов свойств приводит к исключению всех свойств с идентификатором 0x8002, независимо от типа: 
  
 `PROP_TAG(PT_LONG, 0x8002)`
  
Чтобы избежать копирования времени доставки сообщения при копировании сообщения в  другую папку, укажите PR_MESSAGE_DELIVERY_TIME[(PidTagMessageDeliveryTime)](pidtagmessagedeliverytime-canonical-property.md)в теге свойства исключить массив. Чтобы исключить список получателей сообщения, **добавьте свойство PR_MESSAGE_RECIPIENTS** [(PidTagMessageRecipients)](pidtagmessagerecipients-canonical-property.md)в массив исключений. Чтобы исключить вложения сообщения, **добавьте свойство** [PR_MESSAGE_ATTACHMENTS (PidTagMessageAttachments)](pidtagmessageattachments-canonical-property.md)в массив.
  
Аналогично, чтобы предотвратить копирование или перемещение иерархии или таблицы содержимого контейнера папки или адресной **книги,** включите PR_CONTAINER_HIERARCHY [(PidTagContainerHierarchy)](pidtagcontainerhierarchy-canonical-property.md)или **PR_CONTAINER_CONTENTS** [(PidTagContainerContents)](pidtagcontainercontents-canonical-property.md)в массив исключений тега свойств.
  
Игнорируйте MAPI_E_COMPUTED ошибки, возвращаемые в **структуре SPropProblemArray** в _параметре lppProblems._ 
  
Идентификатор интерфейса, на который _указывает lpSrcInterface,_ обычно такой же, как и идентификатор интерфейса, на который указывает _lpDestInterface._ 
  
Если вы передаете допустимый идентификатор интерфейса  _в lpDestInterface,_ но недействительный указатель  _в lpDestObj,_ результаты непредсказуемы. Скорее всего, это приведет к сбой поставщика. 
  
И наоборот, если вам известно о дополнительных сведениях, которые не следует копировать или перемещать, добавьте идентификаторы интерфейса для исключенных интерфейсов в массиве, переданного в _параметре rgiidExclude._ Например, если вы копируете сообщения, но не какие-либо из их вложений сообщений, IID_IMessage в _массиве rgiidExclude._ **DoCopyTo игнорирует** все интерфейсы, указанные в  _rgiidExclude,_ которые он не распознает. 
  
При использовании  _параметра rgiidExclude_ для исключения интерфейса он также исключает все интерфейсы, полученные из этого интерфейса. Например, исключение интерфейса [IMAPIContainer](imapicontainerimapiprop.md) приводит к исключению папок или контейнеров адресной книги в зависимости от типа поставщика. Не исключайте [IMAPIProp](imapipropiunknown.md) или [IUnknown,](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) так как из них вытекает так много интерфейсов. 
  
 **DoCopyTo** сообщает о глобальных ошибках, которые применяются к операции в целом, и об отдельных ошибках, которые применяются к отдельным свойствам. Эти отдельные ошибки помещают в **структуру SPropProblemArray.** Вы можете подавить отчет об ошибках на уровне свойств, передав параметру структуры массива проблем свойств NULL, а не допустимый указатель. 
  
Если вы хотите получить сведения об ошибках, передай допустимый указатель **структуры SPropProblemArray** в _параметре lppProblems._ Когда **DoCopyTo** возвращает S_OK, проверьте возможные ошибки с отдельными свойствами в структуре. Когда **DoCopyTo** возвращает ошибку, в структуре **SPropProblemArray** не возвращается информация. Вместо этого вызовите [метод IMAPISupport::GetLastError,](imapisupport-getlasterror.md) чтобы получить подробные сведения об ошибках. 
  
Если **DoCopyTo** возвращает S_OK, освободите возвращенную структуру **SPropProblemArray,** позвонив функцию [MAPIFreeBuffer.](mapifreebuffer.md) 
  
Если в вызове **DoCopyTo** возникает глобальная ошибка, не используйте или освободите **структуру SPropProblemArray.** Поставщики должны игнорировать _участника ulIndex_ в **структурах SPropProblemArray,** возвращенных **DoCopyTo.**
  
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

