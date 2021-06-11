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

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Копирует или перемещает одно или несколько свойств объекта на другой объект.
  
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

## <a name="parameters"></a>Parameters

 _lpSrcInterface_
  
> [in] Указатель на идентификатор интерфейса (IID), который представляет интерфейс, который будет использоваться для доступа к объекту со свойствами, которые будут скопированы или перемещены.
    
 _lpSrcObj_
  
> [in] Указатель на объект, содержащий свойства, которые будут скопированы или перемещены.
    
 _lpIncludeProps_
  
> [in] Указатель на структуру [SPropTagArray,](sproptagarray.md) которая содержит засчитанный массив тегов свойств, которые указывают свойства копирования или перемещения. Параметр  _lpIncludeProps не_ может быть NULL. 
    
 _ulUIParam_
  
> [in] Ручка родительского окна индикатора прогресса.
    
 _lpProgress_
  
> [in] Указатель на реализацию индикатора прогресса. Если NULL передается в  _параметре lpProgress,_ индикатор прогресса отображается с помощью реализации MAPI. Параметр _lpProgress_ игнорируется, если флаг MAPI_DIALOG в параметре _ulFlags._ 
    
 _lpDestInterface_
  
> [in] Указатель на идентификатор интерфейса, который представляет интерфейс, используемый для доступа к объекту для получения скопированные или перемещенные свойства.
    
 _lpDestObj_
  
> [in] Указатель на объект для получения скопированные или перенесенные свойства.
    
 _ulFlags_
  
> [in] Битмаска флагов, которые контролируют, как выполняется операция копирования или перемещения. Можно установить следующие флаги:
    
MAPI_DIALOG 
  
> Отображает индикатор прогресса.
    
MAPI_MOVE 
  
> **DoCopyProps** должен выполнять операцию перемещения вместо операции копирования. Если этот флаг не установлен, **DoCopyProps** выполняет операцию копирования. 
    
MAPI_NOREPLACE 
  
> Существующие свойства в объекте назначения не должны быть перезаписаны. Если этот флаг не установлен, **DoCopyProps** переопрестит существующие свойства. 
    
 _lppProblems_
  
> [in, out] На входе указатель на указатель на [структуру SPropProblemArray;](spropproblemarray.md) в противном случае NULL, что не указывает на отсутствие необходимости в сведениях об ошибках. Если  _lppProblems_ является допустимым указателем на входе, **DoCopyProps** возвращает подробные сведения об ошибках при копировании одного или более свойств. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Свойства успешно копировали или перемещали.
    
MAPI_E_COLLISION 
  
> Свойство, которое будет скопировано или перемещено, уже существует в объекте назначения, MAPI_NOREPLACE задает флаг. 
    
MAPI_E_FOLDER_CYCLE 
  
> Исходный объект прямо или косвенно содержит объект назначения. Перед обнаружением этого условия, возможно, была выполнена значительная работа, поэтому объекты источника и назначения могут быть частично изменены. 
    
MAPI_E_INTERFACE_NOT_SUPPORTED 
  
> Интерфейс, идентифицированный  _параметром lpSrcInterface,_ не поддерживается исходным объектом, или интерфейс, идентифицированный  _параметром lpDestInterface,_ не поддерживается объектом назначения. 
    
MAPI_E_NO_ACCESS 
  
> Была предпринята попытка доступа к объекту, для которого у вызываемого недостаточно разрешений. Эта ошибка возвращается, если объект назначения является таким же, как и исходный объект.
    
Следующие значения могут быть возвращены в **структуре SPropProblemArray,** но не в качестве возвращаемой величины **для DoCopyProps.** Эти ошибки применимы к одному свойству.
  
MAPI_E_BAD_CHARWIDTH 
  
> Либо был MAPI_UNICODE флаг и **DoCopyProps** не поддерживает Юникод, либо MAPI_UNICODE не был установлен, а **DoCopyProps** поддерживает только Юникод. 
    
MAPI_E_COMPUTED 
  
> Свойство не может быть изменено вызываемой, так как оно является свойством только для чтения, вычисляется владельцем объекта назначения. Эта ошибка не является серьезной; вызываемая должна разрешить продолжение операции копирования.
    
MAPI_E_INVALID_TYPE 
  
> Тип свойства недействителен.
    
MAPI_E_UNEXPECTED_TYPE 
  
> Тип свойства не тот тип, который ожидает вызываемого.
    
## <a name="remarks"></a>Примечания

Метод **IMAPISupport::D oCopyProps** реализован для объектов поддержки поставщиков сообщений. Поставщики магазинов сообщений могут вызвать **DoCopyProps** для реализации метода [IMAPIProp::CopyProps](imapiprop-copyprops.md) для своих папок и сообщений. **DoCopyProps** копирует или перемещает свойства, которые определены в массиве тегов свойств, на которые указывает  _lpIncludeProps_ и которые присутствуют в объекте, на который указывает  _lpSrcObj_. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

При копировании свойств между объектами одного типа, например двумя сообщениями, параметры  _lpSrcInterface_ и  _lpDestInterface_ должны содержать один и тот же идентификатор интерфейса, а параметры  _lpSrcObj_ и  _lpDestObj_ должны указать на объекты одного типа. Если  _lpDestInterface_ задан nULL, **DoCopyProps** возвращает MAPI_E_INVALID_PARAMETER. Если вы установите  _lpDestInterface_ в допустимый идентификатор интерфейса, но установите  _lpDestObj_ недействительным указателем, результаты непредсказуемы. Скорее всего, поставщик не справился с этой услугой. 
  
Установите флаг MAPI_NOREPLACE, если вы не хотите, чтобы какие-либо свойства объекта назначения были перезаписаны. Свойства в объекте назначения, который существует в исходных объектах и не перезаписывается, не удаляются или не изменены.
  
Чтобы скопировать список получателей **сообщения,** включаем свойство [PR_MESSAGE_RECIPIENTS (PidTagMessageRecipients)](pidtagmessagerecipients-canonical-property.md)в массив тегов свойств, на который указывает параметр _lpIncludeProps._ Чтобы скопировать вложения сообщения, **включаем свойство** [PR_MESSAGE_ATTACHMENTS (PidTagMessageAttachments).](pidtagmessageattachments-canonical-property.md) 
  
Чтобы скопировать иерархию или таблицу содержимого контейнера папки или адресной **книги,** включите PR_CONTAINER_HIERARCHY [(PidTagContainerHierarchy)](pidtagcontainerhierarchy-canonical-property.md)или **PR_CONTAINER_CONTENTS** [(PidTagContainerContents)](pidtagcontainercontents-canonical-property.md)в массив тегов свойств. Чтобы включить связанную таблицу содержимого папки, включайте **свойство PR_FOLDER_ASSOCIATED_CONTENTS** [(PidTagFolderAssociatedContents)](pidtagfolderassociatedcontents-canonical-property.md)в массиве.
  
Если подстановки копируется или перемещается, их содержимое копируется или перемещается в полном объеме, независимо от использования свойств, указанных структурой **SPropTagArray.** 
  
 **DoCopyProps** сообщает о глобальных ошибках, которые происходят с операцией в целом, и отдельных ошибках, которые происходят с одним или более свойств. Эти отдельные ошибки помещают в **структуру SPropProblemArray.** Вы можете подавить отчет об ошибках на уровне свойств, передав параметру структуры массива проблем свойств NULL, а не допустимый указатель. 
  
Если вы хотите получить сведения об ошибках, передай допустимый указатель **структуры SPropProblemArray** в _параметре lppProblems._ Когда **DoCopyProps** возвращает S_OK, проверьте возможные ошибки с отдельными свойствами в структуре. Когда **DoCopyProps** возвращает ошибку, в **структуре SPropProblemArray** не возвращается информация. Вместо этого вызовите [метод IMAPISupport::GetLastError,](imapisupport-getlasterror.md) чтобы получить подробные сведения об ошибках. 
  
Если **DoCopyProps** возвращает S_OK, освободите возвращенную структуру **SPropProblemArray,** позвонив в [функцию MAPIFreeBuffer.](mapifreebuffer.md) 
  
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

