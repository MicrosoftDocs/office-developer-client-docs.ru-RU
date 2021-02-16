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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Копирует или перемещает все свойства, кроме специально исключенных.
  
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

## <a name="parameters"></a>Параметры

 _ciidExclude_
  
> [in] Количество интерфейсов, которые необходимо исключить при копировании или перемещении свойств.
    
 _rgiidExclude_
  
> [in] Массив идентификаторов интерфейса (IID), которые указывают интерфейсы, которые не следует использовать при копировании или перемещении дополнительных сведений в объект назначения.
    
 _lpExcludeProps_
  
> [in] Указатель на массив тегов свойств, который определяет теги свойств, которые необходимо исключить из операции копирования или перемещения. Передача **null** в параметр  _lpExcludeProps_ означает, что все свойства объекта должны быть скопированы или перемещены. **CopyTo** возвращает MAPI_E_INVALID_PARAMETER, когда для члена **cValues** структуры [SPropProblemArray,](spropproblemarray.md) на который указывает  _lpExcludeProps,_ установлено 0. 
    
 _ulUIParam_
  
> [in] Handle to the parent window of the progress indicator. 
    
 _lpProgress_
  
> [in] Указатель на реализацию индикатора хода выполнения. Если **в параметре**  _lpProgress_ передается null, MAPI обеспечивает реализацию хода выполнения. Параметр _lpProgress_ игнорируется, если MAPI_DIALOG флага в параметре _ulFlags._ 
    
 _lpInterface_
  
> [in] Указатель на идентификатор интерфейса ( IID), который представляет интерфейс, используемый для доступа к объекту, на который указывает параметр _lpDestObj._ Параметр _lpInterface_ не должен иметь **null.**
    
 _lpDestObj_
  
> [in] Указатель на объект для получения скопированные или перемещенные свойства.
    
 _ulFlags_
  
> [in] Битоваяmas флагов, которая управляет операцией копирования или перемещения. Можно установить следующие флаги:
    
MAPI_DECLINE_OK 
  
> Если **CopyTo вызывает** метод [IMAPISupport::D oCopyTo](imapisupport-docopyto.md) для обработки операции копирования или перемещения, он должен возвращаться немедленно со значением MAPI_E_DECLINE_COPY. MapI MAPI_DECLINE_OK флага для ограничения рекурсии. Клиенты не устанавливают этот флаг. 
    
MAPI_DIALOG 
  
> Отображает индикатор хода выполнения.
    
MAPI_MOVE 
  
> **CopyTo** должен выполнять операцию перемещения вместо операции копирования. Если этот флаг не установлен, **CopyTo выполняет** операцию копирования. 
    
MAPI_NOREPLACE 
  
> Существующие свойства в объекте назначения не следует перезаписывать. Если этот флаг не установлен, **CopyTo** переописает существующие свойства. 
    
 _lppProblems_
  
> [in, out] При вводе указатель на указатель на **структуру SPropProblemArray;** в **противном случае имеется null,** указывающее на отсутствие необходимости в сведениях об ошибках. Если  _lppProblems_ является допустимым указателем при вводе, **CopyTo** возвращает подробные сведения об ошибках при копировании одного или более свойств. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Свойства успешно скопированы или перемещены.
    
MAPI_E_COLLISION 
  
> Подобект нельзя скопировать, так как в объекте назначения уже существует подпроект с таким же отображаемым **именем,** указанным свойством PR_DISPLAY_NAME ([PidTagDisplayName).](pidtagdisplayname-canonical-property.md) 
    
MAPI_E_DECLINE_COPY 
  
> Поставщик услуг не реализует операцию копирования.
    
MAPI_E_FOLDER_CYCLE 
  
> Исходный объект, который выполняет операцию копирования или перемещения прямо или косвенно, содержит объект назначения. Перед обнаружением этого условия могли быть выполнены значительные трудоемкие работы, поэтому исходные и назначения объектов могут быть частично изменены. 
    
MAPI_E_INTERFACE_NOT_SUPPORTED 
  
> Интерфейс, заданный  _параметром lpInterface,_ не поддерживается объектом назначения. 
    
MAPI_E_NO_ACCESS 
  
> Предпринята попытка доступа к объекту, у которого у вызываемого объекта недостаточно разрешений. Эта ошибка возвращается, если объект назначения такой же, как и исходный объект.
    
Следующие значения могут быть возвращены в структуре **SPropProblemArray,** но не в качестве возвращаемой величины **для CopyTo.** К одному свойству применяются следующие ошибки:
  
MAPI_E_BAD_CHARWIDTH 
  
> Либо флаг MAPI_UNICODE установлен, а **CopyTo** не поддерживает Юникод, либо MAPI_UNICODE не установлен, а **CopyTo** поддерживает только Юникод. 
    
MAPI_E_COMPUTED 
  
> Вызываемая не может изменить свойство, так как это свойство, предназначенное только для чтения, вычисленное владельцем конечного объекта. Эта ошибка не является серьезной; Вызываемая должна разрешить продолжение операции копирования.
    
MAPI_E_INVALID_TYPE 
  
> Недопустимый тип свойства.
    
MAPI_E_UNEXPECTED_TYPE 
  
> Тип свойства не является типом, ожидаемым для вызываемого объекта.
    
## <a name="remarks"></a>Примечания

По умолчанию метод **IMAPIProp::CopyTo** копирует или перемещает все свойства текущего объекта в объект назначения. **CopyTo** используется, когда объект должен быть точно скопирован или перемещен, со всеми или большинством его свойств без изменений. 
  
Любые подпроекты в объекте-источнике автоматически включаются в операцию и копируются или перемещаются полностью. По умолчанию **CopyTo** переописает все свойства в объекте назначения, которые соответствуют свойствам из объекта-источника. Если какие-либо из скопированные или перемещенных свойств уже существуют в объекте назначения, существующие свойства перезаписываются новыми свойствами, если в параметре  _ulFlags_ не установлен флаг MAPI_NOREPLACE. Существующие сведения в объекте назначения, который не перезаписан, не будут затронуты. 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Вы можете предоставить полную реализацию **CopyTo** или полагаться на реализацию, предоставляемую MAPI в объекте поддержки. Если вы хотите использовать реализацию MAPI, вызовите **IMAPISupport::D oCopyTo**. Однако если вы делегируете обработку **в DoCopyTo** и передаете флаг MAPI_DECLINE_OK, избегайте вызова в службу поддержки и MAPI_E_DECLINE_COPY. MAPI будет вызываться с этим флагом, чтобы избежать возможной рекурсии, которая может произойти при копировании папок. 
  
Поскольку операция копирования может быть продолжительной, необходимо отобразить индикатор хода выполнения. Используйте [реализацию IMAPIProgress,](imapiprogressiunknown.md) переданную в  _параметре lpProgress,_ если она существует. Если  _lpProgress_ имеет **null,** вызовите метод [IMAPISupport::D oProgressDialog,](imapisupport-doprogressdialog.md) чтобы использовать реализацию MAPI. 
  
Не пытайтесь установить какие-либо известные свойства только для чтения в объекте назначения; вместо MAPI_E_NO_ACCESS возвращается.
  
Исходные и назначения объектов должны использовать одинаковые интерфейсы. Возвращает MAPI_E_INVALID_PARAMETER,  _если lpInterface_ не задан. 
  
Возвращает MAPI_E_INTERFACE_NOT_SUPPORTED, если все известные интерфейсы исключены.
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Не устанавливать флаг MAPI_DECLINE_OK; MAPI использует его в вызовах к реализациям поставщика службы хранения сообщений **CopyTo.** 
  
Поскольку операции копирования и перемещения могут занять некоторое время, следует запросить отображение индикатора хода выполнения, установив MAPI_DIALOG флага. Вы можете установить для _параметра lpProgress_ реализацию **IMAPIProgress**, если она есть, или иметь **null.** Если  _lpProgress_ имеет **значение NULL,** **CopyTo** будет использовать индикатор хода выполнения по умолчанию, который предоставляет MAPI. 
  
Вы можете подавить отображение индикатора хода выполнения, не устанавливая MAPI_DIALOG флага. **CopyTo** игнорирует  _параметры ulUIParam_ и  _lpProgress_ и не отображает индикатор. 
  
 **CopyTo** может сообщать о глобальных и отдельных ошибках или ошибках, которые возникают с одним или более свойствами. Эти отдельные ошибки размещаются в структуре **SPropProblemArray.** Отчеты об ошибках можно подавить на уровне свойства, передав **null** вместо допустимого указателя для параметра структуры массива проблем свойств. 
  
Если вы хотите получить сведения об ошибках, передав допустимый указатель структуры **SPropProblemArray** в _параметре lppProblems._ Когда **CopyTo** возвращает S_OK, проверьте возможные ошибки с отдельными свойствами в структуре. Когда **CopyTo** возвращает ошибку, данные в структуре **SPropProblemArray** не возвращаются. Вместо этого вызовите [IMAPIProp::GetLastError,](imapiprop-getlasterror.md) чтобы получить подробные сведения об ошибке. 
  
Если **CopyTo** возвращает S_OK, освободите возвращенную **структуру SPropProblemArray,** вызывая функцию [MAPIFreeBuffer.](mapifreebuffer.md) 
  
При копировании свойств, уникальных для типа источника объекта, необходимо убедиться, что объект назначения имеет тот же тип. **CopyTo** не препятствует связыванию свойств, которые обычно относятся к одному типу объекта, с другим типом объекта. Вы можете копировать свойства, которые имеют смысл для объекта назначения. Например, не следует копировать свойства сообщения в контейнер адресной книги. 
  
Чтобы обеспечить копирование между объектами одного типа, убедитесь, что источник и объект назначения имеют одинаковый тип, сравнивая указатели объектов или вызывая [IUnknown::QueryInterface.](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) Установите для идентификатора интерфейса, на который указывает  _lpInterface,_ стандартный интерфейс для объекта-источника. Кроме того, убедитесь, что тип или **PR_OBJECT_TYPE** объекта ([PidTagObjectType)](pidtagobjecttype-canonical-property.md)одинаковы для двух объектов. Например, если вы копируете из сообщения, установите для _lpInterface_ IID_IMessage и PR_OBJECT_TYPE для обоих MAPI_MESSAGE.  
  
Если в параметре  _lpDestObj_ передается недопустимый указатель, результаты будут непредсказуемыми. 
  
Исключение свойств при вызове **CopyTo** может быть полезным. Например, некоторые объекты имеют свойства, специфичная для одного экземпляра объекта, например дата и время доставки сообщения. Чтобы избежать копирования времени доставки сообщения при копировании сообщения в другую папку, укажите PR_MESSAGE_DELIVERY_TIME **(** [PidTagMessageDeliveryTime)](pidtagmessagedeliverytime-canonical-property.md)в теге свойства исключить массив. Чтобы исключить список получателей сообщения, добавьте **свойство PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients)](pidtagmessagerecipients-canonical-property.md)в массив исключений. Чтобы исключить вложения сообщения, **добавьте** свойство PR_MESSAGE_ATTACHMENTS [(PidTagMessageAttachments)](pidtagmessageattachments-canonical-property.md)в массив.
  
Аналогичным образом, предотвращают копирование или перемещение иерархии или таблицы содержимого контейнера папки или адресной **книги,** включив PR_CONTAINER_HIERARCHY ([PidTagContainerHierarchy)](pidtagcontainerhierarchy-canonical-property.md)или **PR_CONTAINER_CONTENTS** ([PidTagContainerContents)](pidtagcontainercontents-canonical-property.md)в тег свойства, исключающий массив.
  
Чтобы исключить свойства из операции копирования или перемещения, включаем их теги свойств в параметр _lpExcludeProps._ Если передать результаты **макроса PROP_TAG** для создания тега свойства из определенного идентификатора в массиве тегов свойств, все свойства с этим идентификатором будут исключены. Например, следующая запись в массиве тегов свойств приводит к исключению всех свойств с идентификатором 0x8002, независимо от типа: 
  
 `PROP_TAG(PT_LONG, 0x8002)`
  
Тег **PR_NULL** ([PidTagNull)](pidtagnull-canonical-property.md)нельзя включить в массив _lpExcludeProps._ 
  
Полезность функции **CopyTo** для исключения интерфейсов, возможно, не так очевидна, как полезность исключения свойств. Интерфейс можно исключить при копировании в объект, который не имеет знаний о группе свойств. Например, если скопировать свойства из папки во вложение, вложение сможет работать только с общими свойствами, доступными при любой реализации [IMAPIProp.](imapipropiunknown.md) Исключив [IMAPIFolder](imapifolderimapicontainer.md) из операции копирования, вложение не получит никаких более конкретных свойств папки. 
  
При использовании  _параметра rgiidExclude_ для исключения интерфейса он также исключает все интерфейсы, производные от этого интерфейса. Например, исключение [IMAPIContainer](imapicontainerimapiprop.md) приводит к исключению папок или контейнеров адресной книги в зависимости от типа поставщика. Не исключать **IMAPIProp** или [IUnknown,](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) так как так много интерфейсов являются от них на основе. 
  
Игнорируйте MAPI_E_COMPUTED ошибки, возвращенные в **структуре SPropProblemArray** в _параметре lppProblems._ 
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|File.cpp  <br/> |LoadFromMSG  <br/> |MFCMAPI использует метод **IMAPIProp::CopyTo** для копирования свойств из MSG-файла в объект [IMAPIMessageSite.](imapimessagesiteiunknown.md)  <br/> |
|FolderDlg.cpp  <br/> |CFolderDlg::HandlePaste  <br/> |MFCMAPI использует метод **IMAPIProp::CopyTo** для копирования свойств из сообщения источника в целевое сообщение во время операции в paste.  <br/> |
   
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

