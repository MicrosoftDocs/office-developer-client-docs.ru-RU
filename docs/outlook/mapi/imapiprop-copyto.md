---
title: IMAPIPropCopyTo
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProp.CopyTo
api_type:
- COM
ms.assetid: e56042e9-5bb7-4a99-b6de-1546d4ca07f0
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: f76b0a5482647fe3e181a36d7dcd8cb60ffc8985
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356394"
---
# <a name="imapipropcopyto"></a>IMAPIProp::CopyTo

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Копирует или перемещает все свойства, за исключением специально исключенных свойств.
  
```cpp
HRESULT CopyTo(
 ULONG ciidExclude,
 LPCIID rgiidExclude,
 LPSPropTagArray lpExcludeProps,
 ULONG_PTR ulUIParam,
 LPMAPIPROGRESS lpProgress,
 LPCIID lpInterface,
 LPVOID lpDestObj,
 ULONG ulFlags,
 LPSPropProblemArray FAR * lppProblems
);
```

## <a name="parameters"></a>Parameters

 _ciidExclude_
  
> [in] Количество интерфейсов, исключаемого при копировании или перемещении свойств.
    
 _rgiidExclude_
  
> [in] Массив идентификаторов интерфейса (IID), которые указывают интерфейсы, которые не следует использовать при копировании или перемещении дополнительных сведений в объект назначения.
    
 _lpExcludeProps_
  
> [in] Указатель на массив тегов свойств, который определяет теги свойств, которые следует исключить из операции копирования или перемещения. Передача **null** в  _параметре lpExcludeProps_ указывает на то, что все свойства объекта должны быть скопированы или перемещены. **CopyTo** возвращает MAPI_E_INVALID_PARAMETER, когда член **cValues** структуры [SPropProblemArray,](spropproblemarray.md) на который указывает  _lpExcludeProps,_ задает 0. 
    
 _ulUIParam_
  
> [in] Ручка родительского окна индикатора прогресса. 
    
 _lpProgress_
  
> [in] Указатель на реализацию индикатора прогресса. Если **null** передается в  _параметре lpProgress,_ MAPI обеспечивает реализацию прогресса. Параметр _lpProgress_ игнорируется, если флаг MAPI_DIALOG в параметре _ulFlags._ 
    
 _lpInterface_
  
> [in] Указатель на идентификатор интерфейса (IID), который представляет интерфейс, используемый для доступа к объекту, на который указывает параметр _lpDestObj._ Параметр  _lpInterface_ не должен быть **null**.
    
 _lpDestObj_
  
> [in] Указатель на объект для получения скопированные или перенесенные свойства.
    
 _ulFlags_
  
> [in] Битмашка флагов, которые контролируют операцию копирования или перемещения. Можно установить следующие флаги:
    
MAPI_DECLINE_OK 
  
> Если **CopyTo** вызывает метод [IMAPISupport::D oCopyTo](imapisupport-docopyto.md) для обработки операции копирования или перемещения, он должен немедленно вернуться со значением MAPI_E_DECLINE_COPY. Флажок MAPI_DECLINE_OK mapi, чтобы ограничить повторную рекурсию. Клиенты не устанавливают этот флаг. 
    
MAPI_DIALOG 
  
> Отображает индикатор прогресса.
    
MAPI_MOVE 
  
> **CopyTo** должна выполнять операцию перемещения вместо операции копирования. Если этот флаг не установлен, **CopyTo** выполняет операцию копирования. 
    
MAPI_NOREPLACE 
  
> Существующие свойства в объекте назначения не должны быть перезаписаны. Если этот флаг не установлен, **CopyTo** переописывает существующие свойства. 
    
 _lppProblems_
  
> [in, out] На входе указатель на указатель на **структуру SPropProblemArray;** в **противном случае null**, указывающее отсутствие необходимости в сведениях об ошибках. Если  _lppProblems_ является допустимым указателем ввода, **CopyTo** возвращает подробные сведения об ошибках при копировании одного или более свойств. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Свойства были успешно скопированы или перемещены.
    
MAPI_E_COLLISION 
  
> Субобъект не может быть скопирован, так как в объекте назначения уже существует подобъект с тем же именем **отображения,** заданным свойством [PR_DISPLAY_NAME (PidTagDisplayName).](pidtagdisplayname-canonical-property.md) 
    
MAPI_E_DECLINE_COPY 
  
> Поставщик услуг не реализует операцию копирования.
    
MAPI_E_FOLDER_CYCLE 
  
> Исходный объект, который выполняет операцию копирования или перемещения, прямо или косвенно содержит объект назначения. Перед обнаружением этого условия, возможно, была выполнена значительная работа, поэтому объекты источника и назначения могут быть частично изменены. 
    
MAPI_E_INTERFACE_NOT_SUPPORTED 
  
> Интерфейс, определенные параметром  _lpInterface,_ не поддерживается объектом назначения. 
    
MAPI_E_NO_ACCESS 
  
> Была предпринята попытка доступа к объекту, для которого у вызываемого недостаточно разрешений. Эта ошибка возвращается, если объект назначения является таким же, как и исходный объект.
    
Следующие значения могут быть возвращены в **структуре SPropProblemArray,** но не как значения возврата **для CopyTo**. К одному свойству применяются следующие ошибки:
  
MAPI_E_BAD_CHARWIDTH 
  
> Либо был MAPI_UNICODE флаг, а **CopyTo** не поддерживает Unicode, либо MAPI_UNICODE не установлен, а **CopyTo** поддерживает только Юникод. 
    
MAPI_E_COMPUTED 
  
> Свойство не может быть изменено вызываемой, так как оно является свойством только для чтения, вычисляется владельцем объекта назначения. Эта ошибка не является серьезной; вызываемая должна разрешить продолжение операции копирования.
    
MAPI_E_INVALID_TYPE 
  
> Тип свойства недействителен.
    
MAPI_E_UNEXPECTED_TYPE 
  
> Тип свойства не является типом, ожидаемым вызываемой.
    
## <a name="remarks"></a>Примечания

По умолчанию метод **IMAPIProp::CopyTo** копирует или перемещает все свойства текущего объекта в объект назначения. **CopyTo** используется, когда объект должен быть точно скопирован или перемещен, при этом все или большинство его свойств не повреждены. 
  
Любые подобъекты в исходный объект автоматически включаются в операцию и копируются или перемещаются в полном объеме. По умолчанию **CopyTo** переописывает все свойства в объекте назначения, которые соответствуют свойствам из объекта-источника. Если какие-либо из скопированные или перемещенные свойства уже существуют в объекте назначения, существующие свойства перезаписываются новыми свойствами, если флаг MAPI_NOREPLACE не задан в параметре _ulFlags._ Существующая информация в объекте назначения, который не перезаписан, остается нетронутой. 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Вы можете предоставить полную реализацию **CopyTo** или полагаться на реализацию, которую MAPI предоставляет в объекте поддержки. Если вы хотите использовать реализацию MAPI, позвоните **в IMAPISupport::D oCopyTo**. Однако, если вы делегируете обработку **в DoCopyTo** и вам будет передан MAPI_DECLINE_OK флаг, избегайте вызова поддержки и MAPI_E_DECLINE_COPY. MAPI будет вызывать этот флаг, чтобы избежать возможного повторения, которое может произойти при копировании папок. 
  
Так как операция копирования может быть длительной, необходимо отобразить индикатор прогресса. Используйте [реализацию IMAPIProgress,](imapiprogressiunknown.md) переданную в  _параметре lpProgress,_ если она есть. Если  _lpProgress_ является **null,** позвоните в [метод IMAPISupport::D oProgressDialog](imapisupport-doprogressdialog.md) для использования реализации MAPI. 
  
Не пытайтесь установить какие-либо известные свойства только для чтения в объекте назначения; возвращаем MAPI_E_NO_ACCESS вместо этого.
  
Объекты источника и назначения должны использовать те же интерфейсы. Возврат MAPI_E_INVALID_PARAMETER,  _если lpInterface_ не задан. 
  
Возврат MAPI_E_INTERFACE_NOT_SUPPORTED, если все известные интерфейсы исключены.
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Не установите флаг MAPI_DECLINE_OK; MAPI использует его в своих вызовах для реализации поставщика хранения сообщений **CopyTo.** 
  
Так как операции копирования и перемещения могут занять время, необходимо запросить отображение индикатора прогресса, установив MAPI_DIALOG флага. Вы можете установить  _параметр lpProgress_ для реализации **IMAPIProgress,** если он у вас есть, или **null**. Если  _lpProgress_ **является null,** **CopyTo** будет использовать индикатор прогресса по умолчанию, который предоставляет MAPI. 
  
Вы можете подавить отображение индикатора прогресса, не установив MAPI_DIALOG флага. **CopyTo** игнорирует  _параметры ulUIParam_ и  _lpProgress_ и не отображает индикатор. 
  
 **CopyTo** может сообщать о глобальных и отдельных ошибках или ошибках, которые возникают с одним или более свойствами. Эти отдельные ошибки помещаются в **структуру SPropProblemArray.** Вы можете подавить отчет об ошибках на уровне свойств, передав **null** вместо допустимого указателя для параметра структуры массива проблем свойств. 
  
Если вы хотите получить сведения об ошибках, передай допустимый указатель **структуры SPropProblemArray** в _параметре lppProblems._ Когда **CopyTo** возвращает S_OK, проверьте возможные ошибки с отдельными свойствами в структуре. Когда **CopyTo** возвращает ошибку, в структуре **SPropProblemArray** не возвращается информация. Вместо этого [позвоните в IMAPIProp::GetLastError,](imapiprop-getlasterror.md) чтобы получить подробные сведения об ошибках. 
  
Если **CopyTo** возвращает S_OK, освободите возвращенную структуру **SPropProblemArray,** позвонив в [функцию MAPIFreeBuffer.](mapifreebuffer.md) 
  
Если вы копируете свойства, уникальные для типа исходных объектов, необходимо убедиться, что объект назначения имеет один и тот же тип. **CopyTo** не мешает связывать свойства, которые обычно принадлежат одному типу объекта с другим типом объекта. Вам необходимо скопировать свойства, которые имеют смысл для объекта назначения. Например, не следует копировать свойства сообщений в контейнер адресной книги. 
  
Чтобы убедиться, что объекты одного типа копируют, убедитесь, что источник и объект назначения являются одним и тем же типом, сравнивая указатели объектов или вызывая [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx). Установите идентификатор интерфейса, на который  _указывает lpInterface,_ в стандартный интерфейс для объекта-источника. Кроме того, убедитесь, что **свойство типа или PR_OBJECT_TYPE** объекта [(PidTagObjectType)](pidtagobjecttype-canonical-property.md)является одинаковым для этих двух объектов. Например, если вы скопируете сообщение, установите _lpInterface_  IID_IMessage и PR_OBJECT_TYPE для обоих объектов для MAPI_MESSAGE. 
  
Если недействительный указатель передается в  _параметре lpDestObj,_ результаты непредсказуемы. 
  
Исключение свойств при вызове **CopyTo** может быть полезным. Например, некоторые объекты имеют свойства, определенные одному экземпляру объекта, например дату и время доставки сообщений. Чтобы избежать копирования времени доставки сообщения при копировании сообщения в  другую папку, укажите PR_MESSAGE_DELIVERY_TIME[(PidTagMessageDeliveryTime)](pidtagmessagedeliverytime-canonical-property.md)в теге свойства исключить массив. Чтобы исключить список получателей сообщения, **добавьте свойство PR_MESSAGE_RECIPIENTS** [(PidTagMessageRecipients)](pidtagmessagerecipients-canonical-property.md)в массив исключений. Чтобы исключить вложения сообщения, **добавьте свойство** [PR_MESSAGE_ATTACHMENTS (PidTagMessageAttachments)](pidtagmessageattachments-canonical-property.md)в массив.
  
Аналогичным образом запретить копирование или перемещение иерархии или таблицы содержимого контейнера папки или адресной **книги,** включив PR_CONTAINER_HIERARCHY [(PidTagContainerHierarchy)](pidtagcontainerhierarchy-canonical-property.md)или **PR_CONTAINER_CONTENTS** [(PidTagContainerContents)](pidtagcontainercontents-canonical-property.md)в массив исключений тега свойств.
  
Чтобы исключить свойства из операции копирования или перемещения, включи их теги свойств в параметр _lpExcludeProps._ Если вы передаете результаты **макроса PROP_TAG** для создания тега свойств из определенного идентификатора в массиве тегов свойств, все свойства с этим идентификатором будут исключены. Например, следующая запись в массиве тегов свойств приводит к исключению всех свойств с идентификатором 0x8002, независимо от типа: 
  
 `PROP_TAG(PT_LONG, 0x8002)`
  
Тег **свойства PR_NULL** [(PidTagNull)](pidtagnull-canonical-property.md)не может быть включен в массив _lpExcludeProps._ 
  
Полезность функции **CopyTo** для исключения интерфейсов, возможно, не так очевидна, как полезность исключения свойств. Вы можете исключить интерфейс при копировании объекта, не известного о группе свойств. Например, если скопировать свойства из папки в вложение, единственными свойствами, с которые может работать вложение, являются общие свойства, доступные при любой реализации [IMAPIProp.](imapipropiunknown.md) Исключив [IMAPIFolder](imapifolderimapicontainer.md) из операции копирования, вложение не получит никаких более конкретных свойств папки. 
  
При использовании  _параметра rgiidExclude_ для исключения интерфейса он также исключает все интерфейсы, полученные из этого интерфейса. Например, исключение [IMAPIContainer](imapicontainerimapiprop.md) приводит к исключению папок или контейнеров адресной книги в зависимости от типа поставщика. Не исключайте **IMAPIProp** или [IUnknown,](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) так как из них вытекает так много интерфейсов. 
  
Игнорируйте MAPI_E_COMPUTED ошибки, возвращаемые в **структуре SPropProblemArray** в _параметре lppProblems._ 
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|File.cpp  <br/> |LoadFromMSG  <br/> |MFCMAPI использует метод **IMAPIProp::CopyTo** для копирования свойств из файла .msg в [объект IMAPIMessageSite.](imapimessagesiteiunknown.md)  <br/> |
|FolderDlg.cpp  <br/> |CFolderDlg::HandlePaste  <br/> |MFCMAPI использует **метод IMAPIProp::CopyTo** для копирования свойств из исходных сообщений в целевое сообщение во время операции вклейки.  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPIFolder::CopyMessages](imapifolder-copymessages.md)
  
[IMAPIProp::GetLastError](imapiprop-getlasterror.md)
  
[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)
  
[IMAPIProgress : IUnknown](imapiprogressiunknown.md)
  
[IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md)
  
[IMAPISupport::DoCopyTo](imapisupport-docopyto.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[Каноническое свойство PidTagContainerContents](pidtagcontainercontents-canonical-property.md)
  
[Каноническое свойство PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)
  
[Каноническое свойство PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)
  
[Каноническое свойство PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)
  
[Каноническое свойство PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)
  
[Каноническое свойство PidTagObjectType](pidtagobjecttype-canonical-property.md)
  
[SPropProblemArray](spropproblemarray.md)
  
[SPropTagArray](sproptagarray.md)
  
[IMAPIProp : IUnknown](imapipropiunknown.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

