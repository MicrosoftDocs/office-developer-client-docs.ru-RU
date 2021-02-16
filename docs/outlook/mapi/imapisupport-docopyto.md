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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Копирует или перемещает все свойства одного объекта, кроме специально исключенных, в другой объект.
  
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
  
> [in] Указатель на идентификатор интерфейса ( IID), который представляет интерфейс, который будет использоваться для доступа к объекту, который имеет свойства для копирования или перемещений.
    
 _lpSrcObj_
  
> [in] Указатель на объект, свойства для копирования или перемещении.
    
 _ciidExclude_
  
> [in] Количество интерфейсов, которые необходимо исключить при копировании или перемещение свойств.
    
 _rgiidExclude_
  
> [in] Массив идентификаторов интерфейса, который указывает интерфейсы, которые не следует использовать при копировании или перемещение дополнительных сведений в объект назначения.
    
 _lpExcludeProps_
  
> [in] Указатель на массив тегов свойств, который определяет теги свойств, которые необходимо исключить из операции копирования или перемещения. Передача NULL в параметр  _lpExcludeProps_ означает, что все свойства объекта необходимо скопировать или переместить. **DoCopyTo** возвращает MAPI_E_INVALID_PARAMETER, когда для члена **cValues** структуры [SPropTagArray,](sproptagarray.md) на который указывает  _lpExcludeProps,_ установлено 0. 
    
 _ulUIParam_
  
> [in] Handle to the parent window of the progress indicator. 
    
 _lpProgress_
  
> [in] Указатель на реализацию индикатора хода выполнения. Если в параметре  _lpProgress_ передается NULL, MAPI обеспечивает реализацию хода выполнения. Параметр _lpProgress_ игнорируется, если MAPI_DIALOG флага в параметре _ulFlags._ 
    
 _lpDestInterface_
  
> [in] Указатель на идентификатор интерфейса, который представляет интерфейс, используемый для доступа к объекту для получения скопированные или перемещенные свойства.
    
 _lpDestObj_
  
> [in] Указатель на объект для получения скопированные или перемещенные свойства.
    
 _ulFlags_
  
> [in] Битоваяmas флагов, которая управляет операцией копирования или перемещения. Можно установить следующие флаги:
    
MAPI_DIALOG 
  
> Отображает индикатор хода выполнения. 
    
MAPI_MOVE 
  
> **DoCopyTo** следует выполнить операцию перемещения вместо операции копирования. Если этот флаг не установлен, **DoCopyTo** выполняет операцию копирования. 
    
MAPI_NOREPLACE 
  
> Существующие свойства в объекте назначения не следует перезаписывать. Если этот флаг не установлен, **DoCopyTo** переописает существующие свойства. 
    
 _lppProblems_
  
> [out] При вводе указатель на указатель на [структуру SPropProblemArray;](spropproblemarray.md) в противном случае NULL, что указывает на отсутствие необходимости в сведениях об ошибках. Если  _lppProblems_ является допустимым указателем при вводе, **DoCopyTo** возвращает подробные сведения об ошибках при копировании одного или более свойств. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Свойства успешно скопированы или перемещены.
    
MAPI_E_COLLISION 
  
> Свойство, которое необходимо скопировать или перемещено, уже существует в объекте назначения, MAPI_NOREPLACE установлен флаг. 
    
MAPI_E_FOLDER_CYCLE 
  
> Исходный объект прямо или косвенно содержит объект назначения. Перед обнаружением этого условия могли быть выполнены значительные трудоемкие работы, поэтому исходные и назначения объектов могут быть частично изменены. 
    
MAPI_E_INTERFACE_NOT_SUPPORTED 
  
> Интерфейс, заданный параметром _lpSrcInterface,_ не поддерживается объектом, на который указывает _lpSrcObj,_ или интерфейс, заданный параметром _lpDestInterface,_ не поддерживается объектом, на который указывает _lpDestObj._ 
    
MAPI_E_NO_ACCESS 
  
> Предпринята попытка доступа к объекту, у которого у вызываемого объекта недостаточно разрешений. Эта ошибка возвращается, если объект назначения такой же, как и исходный объект.
    
MAPI_E_INVALID_PARAMETER 
  
> Параметр  _lpSrcInterface_ имеет NULL. 
    
Следующие значения могут быть возвращены в структуре **SPropProblemArray,** но не в качестве возвращаемой величины **для DoCopyTo.** Эти ошибки относятся к одному свойству.
  
MAPI_E_BAD_CHARWIDTH 
  
> Либо флаг MAPI_UNICODE установлен, а **DoCopyTo** не поддерживает Юникод, либо MAPI_UNICODE не установлен, а **DoCopyTo** поддерживает только Юникод. 
    
MAPI_E_COMPUTED 
  
> Вызываемая не может изменить свойство, так как это свойство, предназначенное только для чтения, вычисляется владельцем конечного объекта. Эта ошибка не является серьезной; Вызываемая должна разрешить продолжение операции копирования.
    
MAPI_E_INVALID_TYPE 
  
> Недопустимый тип свойства.
    
MAPI_E_UNEXPECTED_TYPE 
  
> Тип свойства не является типом, ожидаемым для вызываемого объекта.
    
## <a name="remarks"></a>Примечания

Метод **IMAPISupport::D oCopyTo** реализован для объектов поддержки поставщика store сообщений. Поставщики store сообщений могут вызвать **DoCopyTo** для реализации метода [IMAPIProp::CopyTo](imapiprop-copyto.md) для своих папок и сообщений. 
  
По умолчанию **DoCopyTo** копирует или перемещает все свойства одного объекта в другой. Любые подпроекты в объекте-источнике автоматически включаются в операцию и копируются или перемещаются полностью. 
  
Если какие-либо из скопированные или перемещенных свойств уже существуют в объекте назначения, существующие свойства перезаписываются новыми свойствами, если в параметре  _ulFlags_ не установлен флаг MAPI_NOREPLACE. Существующие сведения в объекте назначения, который не перезаписан, не будут затронуты. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Чтобы исключить свойства из операции копирования или перемещения, включаем их теги свойств в параметр _lpExcludeProps._ Если передать результаты использования макроса [PROP_TAG](prop_tag.md) для создания тега свойства из определенного идентификатора в массиве тегов свойств, все свойства с этим идентификатором будут исключены. Например, следующая запись в массиве тегов свойств приводит к исключению всех свойств с идентификатором 0x8002, независимо от типа: 
  
 `PROP_TAG(PT_LONG, 0x8002)`
  
Чтобы избежать копирования времени доставки сообщения при копировании сообщения в другую папку, укажите PR_MESSAGE_DELIVERY_TIME **(** [PidTagMessageDeliveryTime)](pidtagmessagedeliverytime-canonical-property.md)в теге свойства исключить массив. Чтобы исключить список получателей сообщения, добавьте **свойство PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients)](pidtagmessagerecipients-canonical-property.md)в массив исключений. Чтобы исключить вложения сообщения, **добавьте** свойство PR_MESSAGE_ATTACHMENTS [(PidTagMessageAttachments)](pidtagmessageattachments-canonical-property.md)в массив.
  
Аналогичным образом, чтобы предотвратить копирование или перемещение иерархии или таблицы содержимого контейнера папки или адресной книги, включите **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy)](pidtagcontainerhierarchy-canonical-property.md)или **PR_CONTAINER_CONTENTS** ([PidTagContainerContents)](pidtagcontainercontents-canonical-property.md)в тег свойства исключить массив.
  
Игнорируйте MAPI_E_COMPUTED ошибки, возвращенные в **структуре SPropProblemArray** в _параметре lppProblems._ 
  
Идентификатор интерфейса, на который _указывает lpSrcInterface,_ обычно такой же, как идентификатор интерфейса, на который указывает _lpDestInterface._ 
  
Если передать допустимый идентификатор интерфейса в  _lpDestInterface,_ но недопустимый указатель в  _lpDestObj,_ результаты будут непредсказуемыми. Скорее всего, это приведет к сбойу поставщика. 
  
И наоборот, если известно о дополнительных сведениях, которые не следует копировать или перемещать, добавьте идентификаторы интерфейса для интерфейсов, которые необходимо исключить в массиве, передаваемом в _параметре rgiidExclude._ Например, если вы копируете сообщения, но не вложения в них, IID_IMessage массив _rgiidExclude._ **DoCopyTo** игнорирует все интерфейсы, перечисленные в  _rgiidExclude,_ которые не распознают. 
  
При использовании  _параметра rgiidExclude_ для исключения интерфейса он также исключает все интерфейсы, производные от этого интерфейса. Например, исключение интерфейса [IMAPIContainer](imapicontainerimapiprop.md) приводит к исключению папок или контейнеров адресной книги в зависимости от типа поставщика. Не исключать [IMAPIProp](imapipropiunknown.md) или [IUnknown,](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) так как так много интерфейсов являются наивны от них. 
  
 **DoCopyTo** сообщает о глобальных ошибках, которые применяются к операции в целом, и отдельных ошибках, которые применяются к отдельным свойствам. Эти отдельные ошибки помещаются в структуру **SPropProblemArray.** Отчеты об ошибках можно подавить на уровне свойства, передав NULL вместо допустимого указателя для параметра структуры массива проблем свойств. 
  
Если вы хотите получить сведения об ошибках, передав допустимый указатель структуры **SPropProblemArray** в _параметре lppProblems._ Когда **DoCopyTo** возвращает S_OK, проверьте возможные ошибки с отдельными свойствами в структуре. Когда **DoCopyTo** возвращает ошибку, данные в **структуре SPropProblemArray** не возвращаются. Вместо этого вызовите метод [IMAPISupport::GetLastError,](imapisupport-getlasterror.md) чтобы получить подробные сведения об ошибке. 
  
Если **DoCopyTo** возвращает S_OK, освободите возвращенную **структуру SPropProblemArray,** вызывая функцию [MAPIFreeBuffer.](mapifreebuffer.md) 
  
Если при вызове **DoCopyTo** возникает глобальная ошибка, не используйте или не освободите **структуру SPropProblemArray.** Поставщики должны игнорировать член _ulIndex_ в **структурах SPropProblemArray,** возвращаемом **DoCopyTo.**
  
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

