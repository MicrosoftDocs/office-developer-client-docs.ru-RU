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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345509"
---
# <a name="imapipropcopyprops"></a>IMAPIProp::CopyProps

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Копирует или перемещает выбранные свойства. 
  
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

## <a name="parameters"></a>Parameters

 _lpIncludeProps_
  
> [in] Указатель на массив тегов свойств, который указывает свойства для копирования или перемещения. **PR_NULL** [(PidTagNull)](pidtagnull-canonical-property.md)не может быть включена в массив. Параметр  _lpIncludeProps_ не может быть **null**.
    
 _ulUIParam_
  
> [in] Ручка родительского окна индикатора прогресса. 
    
 _lpProgress_
  
> [in] Указатель на реализацию индикатора прогресса. Если **null** передается в  _параметре lpProgress,_ индикатор прогресса отображается с помощью реализации MAPI. Параметр _lpProgress_ игнорируется, если флаг MAPI_DIALOG в параметре _ulFlags._ 
    
 _lpInterface_
  
> [in] Указатель на идентификатор интерфейса (IID), который представляет интерфейс, который должен использоваться для доступа к объекту, на который указывает параметр _lpDestObj._ Параметр  _lpInterface_ не должен быть **null**.
    
 _lpDestObj_
  
> [in] Указатель на объект для получения скопированные или перенесенные свойства.
    
 _ulFlags_
  
> [in] Битмашка флагов, которые контролируют операцию копирования или перемещения. Можно установить следующие флаги:
    
MAPI_DECLINE_OK 
  
> Если **CopyProps** вызывает метод [IMAPISupport::D oCopyProps](imapisupport-docopyprops.md) для обработки операции копирования или перемещения, вместо этого следует немедленно вернуться со значением MAPI_E_DECLINE_COPY. Флажок MAPI_DECLINE_OK mapi, чтобы ограничить повторную рекурсию. Клиенты не устанавливают этот флаг. 
    
MAPI_DIALOG 
  
> Отображает индикатор прогресса.
    
MAPI_MOVE 
  
> **CopyProps** должна выполнять операцию перемещения вместо операции копирования. Если этот флаг не установлен, **CopyProps** выполняет операцию копирования. 
    
MAPI_NOREPLACE 
  
> Существующие свойства в объекте назначения не должны быть перезаписаны. Если этот флаг не установлен, **CopyProps** переопредирует существующие свойства. 
    
 _lppProblems_
  
> [in, out] На входе указатель на указатель на [структуру SPropProblemArray;](spropproblemarray.md) в **противном случае null** указывает на отсутствие необходимости в сведениях об ошибках. Если  _lppProblems_ является допустимым указателем на входе, **CopyProps** возвращает подробные сведения об ошибках при копировании одного или более свойств. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Свойства успешно копировали или перемещали.
    
MAPI_E_COLLISION 
  
> Субобъект не может быть скопирован, так как в объекте назначения уже существует субобъект с тем же именем отображения, определенным свойством **PR_DISPLAY_NAME** [(PidTagDisplayName).](pidtagdisplayname-canonical-property.md) 
    
MAPI_E_DECLINE_COPY 
  
> Поставщик услуг не реализует операцию копирования.
    
MAPI_E_FOLDER_CYCLE 
  
> Исходный объект, который выполняет операцию копирования или перемещения, прямо или косвенно содержит объект назначения. Перед обнаружением этого условия, возможно, была выполнена значительная работа, поэтому объекты источника и назначения могут быть частично изменены. 
    
MAPI_E_INTERFACE_NOT_SUPPORTED 
  
> Интерфейс, определенные параметром  _lpInterface,_ не поддерживается объектом назначения. 
    
MAPI_E_NO_ACCESS 
  
> Была предпринята попытка доступа к объекту, для которого у вызываемого недостаточно разрешений. Эта ошибка возвращается, если объект назначения является таким же, как и исходный объект.
    
Следующие значения могут быть возвращены в **структуре SPropProblemArray,** но не в качестве возвращаемой **величины для CopyProps.** Эти ошибки применимы к одному свойству.
  
MAPI_E_BAD_CHARWIDTH 
  
> Либо флаг MAPI_UNICODE, а **CopyProps** не поддерживает Юникод, либо MAPI_UNICODE не установлен, а **CopyProps** поддерживает только Юникод. 
    
MAPI_E_COMPUTED 
  
> Свойство не может быть изменено вызываемой, так как оно является свойством только для чтения, вычисляется владельцем объекта назначения. Эта ошибка не является серьезной; вызываемая должна разрешить продолжение операции копирования.
    
MAPI_E_INVALID_TYPE 
  
> Тип свойства недействителен.
    
MAPI_E_UNEXPECTED_TYPE 
  
> Тип свойства не является типом, ожидаемым вызываемой.
    
## <a name="remarks"></a>Примечания

Метод **IMAPIProp::CopyProps** копирует или перемещает выбранные свойства из текущего объекта в объект назначения. **CopyProps** используется главным образом для ответа на сообщения и для их переададки, где только некоторые свойства исходного сообщения путешествуют с ответом или переададной копией. 
  
Любые подобъекты в исходный объект автоматически включаются в операцию и копируются или перемещаются в полном объеме независимо от использования свойств, указанных структурой [SPropTagArray.](sproptagarray.md) По умолчанию **CopyProps** переописывает все свойства в объекте назначения, которые соответствуют свойствам из объекта-источника. Если какие-либо из скопированные или перемещенные свойства уже существуют в объекте назначения, существующие свойства перезаписываются новыми свойствами, если флаг MAPI_NOREPLACE не задан в параметре _ulFlags._ Существующая информация в объекте назначения, который не перезаписан, остается нетронутой. 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Вы можете предоставить полную реализацию **CopyProps** или полагаться на реализацию, которую MAPI предоставляет в объекте поддержки. Если вы хотите использовать реализацию MAPI, вызовите **метод IMAPISupport::D oCopyProps.** Однако, если вы делегируете обработку **в DoCopyProps** и вам будет передан флаг MAPI_DECLINE_OK, избеги вызова поддержки и MAPI_E_DECLINE_COPY. Вы будете вызваны с этим флагом MAPI, чтобы избежать возможного повторения, которое может произойти при копировании папок. 
  
Так как операция копирования может быть длительной, необходимо отобразить индикатор прогресса. Используйте [реализацию IMAPIProgress,](imapiprogressiunknown.md) которая передается в  _параметре lpProgress,_ если она есть. Если  _lpProgress_ является **null,** позвоните в [метод IMAPISupport::D oProgressDialog](imapisupport-doprogressdialog.md) для использования реализации MAPI. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Не установите флаг MAPI_DECLINE_OK; он используется MAPI в своих вызовах для реализации поставщика хранения сообщений **CopyProps.** 
  
Поскольку операции копирования и перемещения могут занять время, целесообразно запросить отображение индикатора прогресса, установив MAPI_DIALOG флага. Вы можете установить  _параметр lpProgress_ для реализации **IMAPIProgress,** если он у вас есть, или **null**. Если  _lpProgress_ является **null,** **CopyProps** будет использовать индикатор прогресса по умолчанию, предоставляемый MAPI. 
  
Вы можете подавить отображение индикатора прогресса, не установив MAPI_DIALOG флага. **CopyProps** будет игнорировать  _параметры ulUIParam_ и  _lpProgress_ и избегать отображения индикатора. 
  
 **CopyProps** может сообщать о глобальных и отдельных ошибках или ошибках, которые возникают с одним или более свойств. Эти отдельные ошибки помещают в **структуру SPropProblemArray.** Вы можете подавить отчет об ошибках на уровне свойств, передав **null** вместо допустимого указателя для параметра структуры массива проблем свойств. 
  
Если вы хотите получить сведения об ошибках, передай допустимый указатель **структуры SPropProblemArray** в _параметре lppProblems._ Когда **CopyProps** возвращает S_OK, проверьте возможные ошибки с отдельными свойствами в структуре. Когда **CopyProps** возвращает ошибку, в **структуре SPropProblemArray** не возвращается информация. Вместо этого вызовите [метод IMAPIProp::GetLastError,](imapiprop-getlasterror.md) чтобы получить подробные сведения об ошибках. 
  
Если **CopyProps** возвращает S_OK, освободите возвращенную структуру **SPropProblemArray,** позвонив в [функцию MAPIFreeBuffer.](mapifreebuffer.md) 
  
Если вы копируете свойства, уникальные для типа исходных объектов, необходимо убедиться, что объект назначения имеет один и тот же тип. **CopyProps** не мешает связывать свойства, которые обычно принадлежат одному типу объекта с другим типом объекта. Вам необходимо скопировать свойства, которые имеют смысл для объекта назначения. Например, не следует копировать свойства сообщений в контейнер адресной книги. 
  
Чтобы убедиться, что вы копируете объекты одного типа, убедитесь, что источник и объект назначения являются одним и тем же типом, сравнивая указатели объектов или вызывая метод [IUnknown::QueryInterface.](https://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx) Установите идентификатор интерфейса, на который  _указывает lpInterface,_ в стандартный интерфейс для объекта-источника. Кроме того, убедитесь, что **свойство типа или PR_OBJECT_TYPE** объекта [(PidTagObjectType)](pidtagobjecttype-canonical-property.md)одинаково для этих двух объектов. Например, если вы копируете сообщение, установите _lpInterface_ IID_IMessage  и PR_OBJECT_TYPE для обоих объектов MAPI_MESSAGE. 
  
Если недействительный указатель передается в  _параметре lpDestObj,_ результаты непредсказуемы. 
  
Чтобы скопировать список получателей сообщения, вызывай метод **CopyProps** сообщения и **включив** свойство [PR_MESSAGE_RECIPIENTS (PidTagMessageRecipients)](pidtagmessagerecipients-canonical-property.md)в массив тегов свойств. Чтобы скопировать вложения сообщения, **включаем свойство** [PR_MESSAGE_ATTACHMENTS (PidTagMessageAttachments).](pidtagmessageattachments-canonical-property.md) 
  
Чтобы скопировать иерархию или таблицу содержимого контейнера папки или адресной **книги,** включите свойства PR_CONTAINER_HIERARCHY [(PidTagContainerHierarchy)](pidtagcontainerhierarchy-canonical-property.md)или **PR_CONTAINER_CONTENTS** [(PidTagContainerContents)](pidtagcontainercontents-canonical-property.md)в массиве тегов свойств. Чтобы включить связанную таблицу содержимого папки, включайте **свойство PR_FOLDER_ASSOCIATED_CONTENTS** [(PidTagFolderAssociatedContents)](pidtagfolderassociatedcontents-canonical-property.md)в массиве. 
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|MAPIFunctions.cpp  <br/> |CopyNamedProps  <br/> |MFCMAPI использует **метод IMAPIProp::CopyProps** для копирования именных свойств из одного сообщения в другое.  <br/> |
|SingleMAPIPropListCtrl.cpp  <br/> |CSingleMAPIPropListCtrl::OnPasteProperty  <br/> |MFCMAPI использует **метод IMAPIProp::CopyProps** для вклейки свойства, скопированные с другого объекта.  <br/> |
   
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

