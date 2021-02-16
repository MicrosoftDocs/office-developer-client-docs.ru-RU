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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
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

## <a name="parameters"></a>Параметры

 _lpIncludeProps_
  
> [in] Указатель на массив тегов свойств, который указывает свойства для копирования или перемещения. **PR_NULL** ([PidTagNull)](pidtagnull-canonical-property.md)не могут быть включены в массив. Параметр _lpIncludeProps_ не может иметь **null.**
    
 _ulUIParam_
  
> [in] Handle to the parent window of the progress indicator. 
    
 _lpProgress_
  
> [in] Указатель на реализацию индикатора хода выполнения. Если **в параметре**  _lpProgress_ передается null, индикатор хода выполнения отображается с помощью реализации MAPI. Параметр _lpProgress_ игнорируется, если MAPI_DIALOG флага в параметре _ulFlags._ 
    
 _lpInterface_
  
> [in] Указатель на идентификатор интерфейса ( IID), который представляет интерфейс, который должен использоваться для доступа к объекту, на который указывает параметр _lpDestObj._ Параметр _lpInterface_ не должен иметь **null.**
    
 _lpDestObj_
  
> [in] Указатель на объект для получения скопированные или перемещенные свойства.
    
 _ulFlags_
  
> [in] Битоваяmas флагов, которая управляет операцией копирования или перемещения. Можно установить следующие флаги:
    
MAPI_DECLINE_OK 
  
> Если **CopyProps** вызывает метод [IMAPISupport::D oCopyProps](imapisupport-docopyprops.md) для обработки операции копирования или перемещения, он должен возвращаться немедленно со значением MAPI_E_DECLINE_COPY. MapI MAPI_DECLINE_OK флага для ограничения рекурсии. Клиенты не устанавливают этот флаг. 
    
MAPI_DIALOG 
  
> Отображает индикатор хода выполнения.
    
MAPI_MOVE 
  
> **CopyProps** следует выполнить операцию перемещения вместо операции копирования. Если этот флаг не установлен, **CopyProps** выполняет операцию копирования. 
    
MAPI_NOREPLACE 
  
> Существующие свойства в объекте назначения не следует перезаписывать. Если этот флаг не установлен, **CopyProps** переопредирует существующие свойства. 
    
 _lppProblems_
  
> [in, out] При вводе указатель на указатель на [структуру SPropProblemArray;](spropproblemarray.md) в **противном случае — null,** указывающее на отсутствие необходимости в сведениях об ошибках. Если  _lppProblems_ является допустимым указателем при вводе, **CopyProps** возвращает подробные сведения об ошибках при копировании одного или более свойств. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Свойства успешно скопированы или перемещены.
    
MAPI_E_COLLISION 
  
> Подобект нельзя скопировать, так как в объекте назначения уже существует подпроект с таким же отображаемым именем, определенным свойством **PR_DISPLAY_NAME** ([PidTagDisplayName).](pidtagdisplayname-canonical-property.md) 
    
MAPI_E_DECLINE_COPY 
  
> Поставщик услуг не реализует операцию копирования.
    
MAPI_E_FOLDER_CYCLE 
  
> Исходный объект, который выполняет операцию копирования или перемещения прямо или косвенно, содержит объект назначения. Перед обнаружением этого условия могли быть выполнены значительные трудоемкие работы, поэтому исходные и назначения объектов могут быть частично изменены. 
    
MAPI_E_INTERFACE_NOT_SUPPORTED 
  
> Интерфейс, заданный  _параметром lpInterface,_ не поддерживается объектом назначения. 
    
MAPI_E_NO_ACCESS 
  
> Предпринята попытка доступа к объекту, у которого у вызываемого объекта недостаточно разрешений. Эта ошибка возвращается, если объект назначения такой же, как и исходный объект.
    
Следующие значения могут быть возвращены в структуре **SPropProblemArray,** но не в качестве возвращаемой величины **для CopyProps.** Эти ошибки относятся к одному свойству.
  
MAPI_E_BAD_CHARWIDTH 
  
> Либо флаг MAPI_UNICODE установлен, а **CopyProps** не поддерживает Юникод, либо MAPI_UNICODE не установлен, а **CopyProps** поддерживает только Юникод. 
    
MAPI_E_COMPUTED 
  
> Вызываемая не может изменить свойство, так как это свойство, предназначенное только для чтения, вычисленное владельцем конечного объекта. Эта ошибка не является серьезной; Вызываемая должна разрешить продолжение операции копирования.
    
MAPI_E_INVALID_TYPE 
  
> Недопустимый тип свойства.
    
MAPI_E_UNEXPECTED_TYPE 
  
> Тип свойства не является типом, ожидаемым для вызываемого объекта.
    
## <a name="remarks"></a>Примечания

Метод **IMAPIProp::CopyProps** копирует или перемещает выбранные свойства из текущего объекта в объект назначения. **CopyProps** используется главным образом для ответов на сообщения и переадовки сообщений, где только некоторые свойства исходного сообщения перенаправят с ответом или перенапраздной копией. 
  
Любые подобъекты в объекте-источнике автоматически включаются в операцию и копируются или перемещаются полностью независимо от использования свойств, указанных в структуре [SPropTagArray.](sproptagarray.md) По умолчанию **CopyProps** переописает все свойства в объекте назначения, которые соответствуют свойствам из объекта-источника. Если какие-либо из скопированные или перемещенных свойств уже существуют в объекте назначения, существующие свойства перезаписываются новыми свойствами, если в параметре  _ulFlags_ не установлен флаг MAPI_NOREPLACE. Существующие сведения в объекте назначения, который не перезаписан, не будут затронуты. 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Вы можете предоставить полную реализацию **CopyProps** или полагаться на реализацию, предоставляемую MAPI в объекте поддержки. Если вы хотите использовать реализацию MAPI, вызовите метод **IMAPISupport::D oCopyProps.** Однако если вы делегируете обработку **в DoCopyProps** и передаете флаг MAPI_DECLINE_OK, избегайте вызова в службу поддержки и MAPI_E_DECLINE_COPY. MAPI будет вызван с этим флагом, чтобы избежать возможной рекурсии, которая может произойти при копировании папок. 
  
Поскольку операция копирования может быть продолжительной, необходимо отобразить индикатор хода выполнения. Используйте [реализацию IMAPIProgress,](imapiprogressiunknown.md) которая передается в  _параметре lpProgress,_ если она существует. Если  _lpProgress_ имеет **null,** вызовите метод [IMAPISupport::D oProgressDialog,](imapisupport-doprogressdialog.md) чтобы использовать реализацию MAPI. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Не устанавливать флаг MAPI_DECLINE_OK; он используется MAPI в вызовах к реализациям **поставщика службы copyProps** для хранения сообщений. 
  
Поскольку операции копирования и перемещения могут занять некоторое время, разумно запросить отображение индикатора хода выполнения, установив MAPI_DIALOG флага. Вы можете установить для _параметра lpProgress_ реализацию **IMAPIProgress**, если она есть, или иметь **null.** Если  _lpProgress_ имеет **значение NULL,** **CopyProps** будет использовать индикатор хода выполнения по умолчанию, предоставленный MAPI. 
  
Вы можете подавить отображение индикатора хода выполнения, не устанавливая MAPI_DIALOG флага. **CopyProps** игнорирует  _параметры ulUIParam_ и  _lpProgress_ и не отображает индикатор. 
  
 **CopyProps** может сообщать о глобальных и отдельных ошибках или ошибках, которые возникают с одним или более свойствами. Эти отдельные ошибки помещаются в структуру **SPropProblemArray.** Отчеты об ошибках можно подавить на уровне свойства, передав **null** вместо допустимого указателя для параметра структуры массива проблем свойств. 
  
Если вы хотите получить сведения об ошибках, передав допустимый указатель структуры **SPropProblemArray** в _параметре lppProblems._ Когда **CopyProps** возвращает S_OK, проверьте возможные ошибки с отдельными свойствами в структуре. Когда **CopyProps** возвращает ошибку, данные в структуре **SPropProblemArray** не возвращаются. Вместо этого вызовите метод [IMAPIProp::GetLastError,](imapiprop-getlasterror.md) чтобы получить подробные сведения об ошибке. 
  
Если **CopyProps** возвращает S_OK, освободите возвращенную **структуру SPropProblemArray,** вызывая функцию [MAPIFreeBuffer.](mapifreebuffer.md) 
  
При копировании свойств, уникальных для типа источника объекта, необходимо убедиться, что объект назначения имеет тот же тип. **CopyProps** не препятствует связыванию свойств, которые обычно относятся к одному типу объекта, с другим типом объекта. Вы можете копировать свойства, которые имеют смысл для объекта назначения. Например, не следует копировать свойства сообщения в контейнер адресной книги. 
  
Чтобы убедиться, что вы копируете объекты одного типа, убедитесь, что источник и объект назначения имеют одинаковый тип, сравнивая указатели объектов или вызывая метод [IUnknown::QueryInterface.](https://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx) Установите для идентификатора интерфейса, на который указывает  _lpInterface,_ стандартный интерфейс для объекта-источника. Кроме того, убедитесь, что тип или **PR_OBJECT_TYPE** объекта ([PidTagObjectType)](pidtagobjecttype-canonical-property.md)одинаковы для двух объектов. Например, если вы копируете из сообщения, установите для _lpInterface_ IID_IMessage и PR_OBJECT_TYPE для обоих объектов MAPI_MESSAGE.  
  
Если в параметре  _lpDestObj_ передается недопустимый указатель, результаты будут непредсказуемыми. 
  
Чтобы скопировать список получателей сообщения, вызовите метод **CopyProps** сообщения и включим свойство **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients)](pidtagmessagerecipients-canonical-property.md)в массив тегов свойств. Чтобы скопировать вложения сообщения, **включаем свойство PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments).](pidtagmessageattachments-canonical-property.md) 
  
Чтобы скопировать иерархию или таблицу содержимого контейнера папки или адресной книги, включите свойства **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy)](pidtagcontainerhierarchy-canonical-property.md)или **PR_CONTAINER_CONTENTS** ([PidTagContainerContents)](pidtagcontainercontents-canonical-property.md)в массив тегов свойств. Чтобы включить связанную с папкой таблицу содержимого, включайте **свойство PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents)](pidtagfolderassociatedcontents-canonical-property.md)в массив. 
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|MAPIFunctions.cpp  <br/> |CopyNamedProps  <br/> |MFCMAPI использует метод **IMAPIProp::CopyProps** для копирования именуемого свойства из одного сообщения в другое.  <br/> |
|SingleMAPIPropListCtrl.cpp  <br/> |CSingleMAPIPropListCtrl::OnPasteProperty  <br/> |MFCMAPI использует метод **IMAPIProp::CopyProps,** чтобы вкопировать свойство, скопированные из другого объекта.  <br/> |
   
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

