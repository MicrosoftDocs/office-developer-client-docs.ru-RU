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
ms.openlocfilehash: 24107ae1926c8590da6a823a354eeae72d72f248
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405585"
---
# <a name="imapisupportdocopyprops"></a>IMAPISupport::DoCopyProps

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Копирует или перемещает одно или несколько свойств объекта в другой объект.
  
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
  
> [in] Указатель на идентификатор интерфейса ( IID), который представляет интерфейс, который будет использоваться для доступа к объекту со свойствами, которые необходимо скопировать или переместить.
    
 _lpSrcObj_
  
> [in] Указатель на объект, содержащий свойства для копирования или перемещений.
    
 _lpIncludeProps_
  
> [in] Указатель на структуру [SPropTagArray,](sproptagarray.md) которая содержит подсчетный массив тегов свойств, которые указывают свойства для копирования или перемещения. Параметр  _lpIncludeProps_ не может иметь NULL. 
    
 _ulUIParam_
  
> [in] Handle to the parent window of the progress indicator.
    
 _lpProgress_
  
> [in] Указатель на реализацию индикатора хода выполнения. Если в параметре  _lpProgress_ передается NULL, индикатор хода выполнения отображается с помощью реализации MAPI. Параметр _lpProgress_ игнорируется, если MAPI_DIALOG флага в параметре _ulFlags._ 
    
 _lpDestInterface_
  
> [in] Указатель на идентификатор интерфейса, который представляет интерфейс, используемый для доступа к объекту для получения скопированные или перемещенные свойства.
    
 _lpDestObj_
  
> [in] Указатель на объект для получения скопированные или перемещенные свойства.
    
 _ulFlags_
  
> [in] Битоваяmas флагов, которая управляет выполнением операции копирования или перемещения. Можно установить следующие флаги:
    
MAPI_DIALOG 
  
> Отображает индикатор хода выполнения.
    
MAPI_MOVE 
  
> **DoCopyProps** должен выполнять операцию перемещения вместо операции копирования. Если этот флаг не установлен, **DoCopyProps** выполняет операцию копирования. 
    
MAPI_NOREPLACE 
  
> Существующие свойства в объекте назначения не следует перезаписывать. Если этот флаг не установлен, **DoCopyProps** переопредирует существующие свойства. 
    
 _lppProblems_
  
> [in, out] При вводе указатель на указатель на [структуру SPropProblemArray;](spropproblemarray.md) в противном случае NULL, что указывает на отсутствие необходимости в сведениях об ошибках. Если  _lppProblems_ является допустимым указателем при вводе, **DoCopyProps** возвращает подробные сведения об ошибках при копировании одного или более свойств. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Свойства были успешно скопированы или перемещены.
    
MAPI_E_COLLISION 
  
> Свойство, которое необходимо скопировать или сдвинуто, уже существует в объекте назначения, MAPI_NOREPLACE установлен флаг. 
    
MAPI_E_FOLDER_CYCLE 
  
> Исходный объект прямо или косвенно содержит объект назначения. Перед обнаружением этого условия могли быть выполнены значительные трудоемкие работы, поэтому исходные и назначения объектов могут быть частично изменены. 
    
MAPI_E_INTERFACE_NOT_SUPPORTED 
  
> Интерфейс, заданный параметром  _lpSrcInterface,_ не поддерживается исходным объектом, или интерфейс, заданный параметром  _lpDestInterface,_ не поддерживается объектом назначения. 
    
MAPI_E_NO_ACCESS 
  
> Предпринята попытка доступа к объекту, у которого у вызываемого объекта недостаточно разрешений. Эта ошибка возвращается, если объект назначения такой же, как и исходный объект.
    
Следующие значения могут быть возвращены в структуре **SPropProblemArray,** но не в качестве возвращаемой величины **для DoCopyProps.** Эти ошибки относятся к одному свойству.
  
MAPI_E_BAD_CHARWIDTH 
  
> Либо флаг MAPI_UNICODE установлен, а **DoCopyProps** не поддерживает Юникод, либо MAPI_UNICODE не установлен, и **DoCopyProps** поддерживает только Юникод. 
    
MAPI_E_COMPUTED 
  
> Вызываемая не может изменить свойство, так как это свойство, предназначенное только для чтения, вычисляется владельцем конечного объекта. Эта ошибка не является серьезной; Вызываемая должна разрешить продолжение операции копирования.
    
MAPI_E_INVALID_TYPE 
  
> Недопустимый тип свойства.
    
MAPI_E_UNEXPECTED_TYPE 
  
> Тип свойства не является типом, который ожидает вызываемая.
    
## <a name="remarks"></a>Примечания

Метод **IMAPISupport::D oCopyProps** реализован для объектов поддержки поставщика службы хранения сообщений. Поставщики store сообщений могут вызывать **DoCopyProps** для реализации метода [IMAPIProp::CopyProps](imapiprop-copyprops.md) для своих папок и сообщений. **DoCopyProps** копирует или перемещает свойства, которые определены в массиве тегов свойств, на которые указывает _lpIncludeProps_ и которые присутствуют в объекте, на который указывает _lpSrcObj._ 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

При копировании свойств между объектами одного типа, например двумя сообщениями,  _параметры lpSrcInterface_ и  _lpDestInterface_ должны содержать один и тот же идентификатор интерфейса, а  _параметры lpSrcObj_ и  _lpDestObj_ должны указать объекты одного типа. Если  _для lpDestInterface задано_ NULL, **DoCopyProps** возвращает MAPI_E_INVALID_PARAMETER. Если для  _lpDestInterface задан_ допустимый идентификатор интерфейса, но для  _lpDestObj_ задан недопустимый указатель, результаты будут непредсказуемыми. Скорее всего, поставщик не будет работать. 
  
Установите флаг MAPI_NOREPLACE, если не нужно перезаписывать какие-либо свойства в объекте назначения. Свойства в объекте назначения, которые существуют в объекте-источнике и не перезаписываются, не удаляются и не изменяются.
  
Чтобы скопировать список получателей сообщения, включаем свойство **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients)](pidtagmessagerecipients-canonical-property.md)в массив тегов свойств, на который указывает параметр _lpIncludeProps._ Чтобы скопировать вложения сообщения, **включаем свойство PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments).](pidtagmessageattachments-canonical-property.md) 
  
Чтобы скопировать иерархию или таблицу содержимого контейнера папки или адресной книги, включите **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy)](pidtagcontainerhierarchy-canonical-property.md)или **PR_CONTAINER_CONTENTS** ([PidTagContainerContents)](pidtagcontainercontents-canonical-property.md)в массив тегов свойств. Чтобы включить связанную с папкой таблицу содержимого, включайте **свойство PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents)](pidtagfolderassociatedcontents-canonical-property.md)в массив.
  
Если вупапки копируется или перемещается, их содержимое копируется или перемещается полностью независимо от использования свойств, указанных в **структуре SPropTagArray.** 
  
 **DoCopyProps** сообщает о глобальных ошибках, которые возникают с помощью операции в целом, и отдельных ошибках, которые возникают с одним или более свойствами. Эти отдельные ошибки помещаются в структуру **SPropProblemArray.** Отчеты об ошибках можно подавить на уровне свойства, передав NULL вместо допустимого указателя для параметра структуры массива проблем свойств. 
  
Если вы хотите получить сведения об ошибках, передав допустимый указатель структуры **SPropProblemArray** в _параметре lppProblems._ Когда **DoCopyProps** возвращает S_OK, проверьте возможные ошибки с отдельными свойствами в структуре. Когда **DoCopyProps** возвращает ошибку, данные в структуре **SPropProblemArray** не возвращаются. Вместо этого вызовите метод [IMAPISupport::GetLastError,](imapisupport-getlasterror.md) чтобы получить подробные сведения об ошибке. 
  
Если **DoCopyProps** возвращает S_OK, освободите возвращенную **структуру SPropProblemArray,** вызывая функцию [MAPIFreeBuffer.](mapifreebuffer.md) 
  
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

