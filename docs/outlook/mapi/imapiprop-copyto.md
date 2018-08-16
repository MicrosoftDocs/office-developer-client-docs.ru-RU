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
ms.openlocfilehash: aa2869b1e3495bfb8a431e79a55d11a1ee1c5ca6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809026"
---
# <a name="imapipropcopyto"></a>IMAPIProp::CopyTo

  
  
**Относится к**: Outlook 
  
Копирует или переносит все свойства, за исключением специально исключенные свойства.
  
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
  
> [in] Число интерфейсов следует исключить при копировании или перемещении свойства.
    
 _rgiidExclude_
  
> [in] Массив идентификаторов интерфейса (идентификаторы IID), которые определяют интерфейсы, которые не должны использоваться при дополнительную информацию, копируется или переносится в целевой объект.
    
 _lpExcludeProps_
  
> [in] Указатель в массив тег свойства, который определяет свойство теги, которые следует исключить из копии или операции перемещения. Передача **значение null,** с помощью параметра _lpExcludeProps_ означает, что все свойства объекта следует скопировать или переместить. **CopyTo** возвращает MAPI_E_INVALID_PARAMETER при член **cValues** структуры [SPropProblemArray](spropproblemarray.md) указывает _lpExcludeProps_ имеет значение 0. 
    
 _ulUIParam_
  
> [in] Дескриптор родительского окна индикатор хода выполнения. 
    
 _lpProgress_
  
> [in] Указатель на реализацию индикатор хода выполнения. Если **значение null,** передается в параметре _lpProgress_ , MAPI предоставляет реализацию хода выполнения. Параметр _lpProgress_ игнорируется, пока флаг MAPI_DIALOG будет выполнен с помощью параметра _ulFlags_ . 
    
 _lpInterface_
  
> [in] Указатель на идентификатор интерфейса (ИД интерфейса), который представляет интерфейс, который будет использоваться для доступа к объекту, на который указывает параметр _lpDestObj_ . Параметр _lpInterface_ не должно быть **значение null**.
    
 _lpDestObj_
  
> [in] Указатель на объект для получения свойств копируемые или перемещения.
    
 _ulFlags_
  
> [in] Битовая маска флаги, который определяет операцию копирования или перемещения. Можно задать следующие флажки:
    
MAPI_DECLINE_OK 
  
> Если **CopyTo** вызывает метод [IMAPISupport::DoCopyTo](imapisupport-docopyto.md) для обработки копировать или перемещать операции, она немедленно вместо этого возвращает со значением ошибки MAPI_E_DECLINE_COPY. Флаг MAPI_DECLINE_OK задается MAPI для ограничения рекурсии. Клиенты не задан этот флаг. 
    
MAPI_DIALOG 
  
> Отображает индикатор хода выполнения.
    
MAPI_MOVE 
  
> **CopyTo** следует выполнять операции перемещения вместо операцию копирования. Если этот флаг не задан, **CopyTo** выполняет операцию копирования. 
    
MAPI_NOREPLACE 
  
> Не следует перезаписывать существующие свойства в целевой объект. Если этот флаг не задан, **CopyTo** перезаписывает существующие свойства. 
    
 _lppProblems_
  
> [in, out] На входе указатель указатель на структуру **SPropProblemArray** ; в противном случае — **значение null**, указывает, не требуется выполнять сведения об ошибке. Если _lppProblems_ допустимый указатель на входные данные, **CopyTo** возвращает подробные сведения об ошибках в копирование одного или нескольких свойств. 
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> Свойства успешно копирования или перемещения.
    
MAPI_E_COLLISION 
  
> Вложенные объекты, которые не могут быть скопированы, так как вложенные объекты с тем же отображаемое имя, заданное свойством **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) — уже существует в целевой объект. 
    
MAPI_E_DECLINE_COPY 
  
> Поставщик услуг не реализует операцию копирования.
    
MAPI_E_FOLDER_CYCLE 
  
> Исходный объект для выполнения операции копирования или перемещения прямо или косвенно содержит целевой объект. Важные может быть выполнено перед был обнаружен это условие, поэтому исходный и целевой объекты частично могут быть изменены. 
    
MAPI_E_INTERFACE_NOT_SUPPORTED 
  
> Интерфейс, определенного параметром _lpInterface_ не поддерживается в целевой объект. 
    
MAPI_E_NO_ACCESS 
  
> Предпринята попытка получить доступ к объекту, для которого вызывающий не имеет разрешений. Эта ошибка возвращается в том случае, если в целевой объект совпадает с исходным объектом.
    
Возможные значения могут быть возвращены в структуре **SPropProblemArray** , но не как возвращаемые значения для **CopyTo**. Следующие ошибки относятся к одному свойству:
  
MAPI_E_BAD_CHARWIDTH 
  
> Либо был установлен флажок MAPI_UNICODE и **CopyTo** не поддерживает Юникод, или MAPI_UNICODE не было установлено и **CopyTo** поддерживает только Юникод. 
    
MAPI_E_COMPUTED 
  
> Невозможно изменить свойство вызывающим абонентом, так как он является свойством только для чтения, вычисленный владельцем конечного объекта. Эта ошибка не является очень неблагоприятных; вызывающего абонента, должна поддерживать операции копирования для продолжения.
    
MAPI_E_INVALID_TYPE 
  
> Недопустимый тип свойства.
    
MAPI_E_UNEXPECTED_TYPE 
  
> Тип свойства не типа, вызывающего абонента.
    
## <a name="remarks"></a>Замечания

По умолчанию метод **IMAPIProp::CopyTo** копирует или переносит все свойства текущего объекта в конечный объект. **CopyTo** используется, когда объект следует скопировать или переместить точно, со всех или большая часть их свойств без изменений. 
  
Вложенными объектами в объекте источника автоматически включается в операцию и перемещаются или копируются полностью. По умолчанию **CopyTo** перезаписывает любые свойства в целевом объекте, соответствующие свойства из исходного объекта. Если какие-либо свойства скопированной или перемещенной уже существует в целевом объекте, существующие свойства перезаписываются новых свойств, пока флаг MAPI_NOREPLACE будет выполнен с помощью параметра _ulFlags_ . Существующие данные в целевой объект, который не перезаписывается остаются без изменений. 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Можно предоставить полная реализация **CopyTo** или зависеть от реализации, предоставляющий MAPI в своем объекте поддержки. Если вы хотите использовать в реализации интерфейса MAPI, вызовите **IMAPISupport::DoCopyTo**. Если делегирование обработки для **DoCopyTo** и передаются флаг MAPI_DECLINE_OK, избежать вызова поддержки и вместо этого возвращать MAPI_E_DECLINE_COPY. MAPI выполняется звонок с помощью этот флаг, чтобы избежать возможных рекурсии, которая может произойти при копировании папки. 
  
Так как операция копирования может быть длинным, должны отображать индикатор хода выполнения. Используйте реализации [IMAPIProgress](imapiprogressiunknown.md) , переданной в параметре _lpProgress_ , если он существует. Если _lpProgress_ имеет **значение null**, вызовите метод [IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md) для использования в реализации интерфейса MAPI. 
  
Не пытайтесь задать все известные свойства только для чтения в целевом объекте; Вместо этого возвратите MAPI_E_NO_ACCESS.
  
Исходный и целевой объекты следует использовать те же интерфейсы. Возвращает MAPI_E_INVALID_PARAMETER, если _lpInterface_ не задано. 
  
Возвращает MAPI_E_INTERFACE_NOT_SUPPORTED, если не включены все известные интерфейсы.
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Не задан флаг MAPI_DECLINE_OK; MAPI используется в его вызовы для сообщения **CopyTo** реализации поставщика хранилища. 
  
Так как операции копирования и перемещения может потребоваться времени, путем установки флага MAPI_DIALOG должен запрашивать отображения индикатора хода выполнения. Можно задать параметр _lpProgress_ для внедрения **IMAPIProgress**, если такой существует, или значение **null**. Если _lpProgress_ имеет **значение null**, **CopyTo** будет использовать индикатор хода выполнения по умолчанию, который предоставляет MAPI. 
  
Можно отключить отображение индикатора хода выполнения, не задав флаг MAPI_DIALOG. **CopyTo** будет игнорировать параметры _ulUIParam_ и _lpProgress_ и не будет отображаться значок. 
  
 **CopyTo** можно сообщить о глобальном уровне и на отдельные ошибки или ошибки, возникающие при работе с одного или нескольких свойств. Эти отдельные ошибки помещаются в структуре **SPropProblemArray** . Отчеты на уровне свойств, передав **значение null**, а не является допустимым указателем, для параметра свойство массива проблема структура об ошибках, можно отключить. 
  
Если вы хотите получать сведения об ошибках, передайте допустимый указатель структура **SPropProblemArray** с помощью параметра _lppProblems_ . При **CopyTo** возвращает значение S_OK, проверьте наличие возможных ошибок с помощью отдельных свойств в структуре. Когда **CopyTo** возвращает ошибку, не информация возвращается в структуре **SPropProblemArray** . Вместо этого вызов [IMAPIProp::GetLastError](imapiprop-getlasterror.md) , чтобы получить подробные сведения об ошибке. 
  
Если **CopyTo** возвращает значение S_OK, освободите возвращенные структура **SPropProblemArray** путем вызова функции [MAPIFreeBuffer](mapifreebuffer.md) . 
  
При копировании свойств, которые являются уникальными для тип объекта, необходимо убедиться, что в целевой объект является одного типа. **CopyTo** не запрещает связывания свойства, которые обычно относятся к один тип объекта, с другой тип объекта. Зависит от пользователя для копирования свойств, которые нужны для конечного объекта. К примеру не следует копировать свойства сообщений к контейнеру адресной книги. 
  
Чтобы скопировать между объектами одного типа, убедитесь, что установлен исходный и конечный объект того же типа, путем сравнения указателей объектов или вызов [IUnknown::QueryInterface](http://msdn.microsoft.com/en-us/library/ms682521%28v=VS.85%29.aspx). Задайте идентификатор интерфейса, на который указывает _lpInterface_ стандартный интерфейс для объекта источника. Кроме того убедитесь, что тип объекта или свойство **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)) является общим для двух объектов. Например при копировании из сообщения, задайте _lpInterface_ IID_IMessage и **PR_OBJECT_TYPE** объекты MAPI_MESSAGE. 
  
Если недопустимый указатель передается в параметре _lpDestObj_ , результаты непредсказуемы. 
  
Исключение свойств на **CopyTo** звонка можно использовать. Например некоторые объекты имеют свойства, которые специфичны для одного экземпляра объекта, таких как дата и время доставки сообщения. Чтобы предотвратить копирование время доставки сообщений, при копировании сообщения в другую папку, укажите **PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)) в массиве свойство tag исключить. Чтобы исключить список получателей сообщения, добавьте свойство **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) в массиве исключить. Чтобы исключить вложений сообщений, добавьте свойство **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) в массиве.
  
Аналогично предотвратить копирование или перемещение папки или иерархии или содержимое таблицы контейнер адресной книги, включая **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) или **PR_CONTAINER_CONTENTS** ([ PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) в свойстве тег исключить массива.
  
Чтобы исключить свойства из копии или операции перемещения, включают теги их свойства с помощью параметра _lpExcludeProps_ . При передаче результаты макрос **PROP_TAG** для построения тега свойства из указанный идентификатор в массиве тега свойства будут исключены все свойства с этим идентификатором. Например следующую запись в массиве тега свойства вызывает все свойства с идентификатором 0x8002, чтобы исключить, независимо от типа: 
  
 `PROP_TAG(PT_LONG, 0x8002)`
  
Тег свойства **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) нельзя включить в массиве _lpExcludeProps_ . 
  
Полезность функции **CopyTo** для исключения интерфейсы не может быть очевидные полезность исключение свойств. Интерфейс можно исключить при копировании объект, который не знает группа свойств. Например при копировании свойств из папки вложения, только свойства, которые вложение может работать с: общие свойства, доступные с любой реализации [IMAPIProp](imapipropiunknown.md) . Исключив [IMAPIFolder](imapifolderimapicontainer.md) из операции копирования, вложение не будет получать более детальную свойства папки. 
  
Если используется параметр _rgiidExclude_ следует исключить интерфейс также исключаются все интерфейсы, производные от этого интерфейса. Например за исключением [IMAPIContainer](imapicontainerimapiprop.md) включен, папки или контейнеров адресной книги для исключения, в зависимости от типа поставщика. Не исключить **IMAPIProp** или [IUnknown](http://msdn.microsoft.com/en-us/library/ms680509%28v=VS.85%29.aspx) из-за слишком большом числе интерфейсы производные от них. 
  
Пропуск MAPI_E_COMPUTED ошибок, возвращаемых в структуре **SPropProblemArray** в параметре _lppProblems_ . 
  
## <a name="mfcmapi-reference"></a>Справочник по mfcmapi (en)

������ ���� mfcmapi (en) ���������� � ������� ����.
  
|**����**|**�������**|**�����������**|
|:-----|:-----|:-----|
|File.cpp  <br/> |LoadFromMSG  <br/> |Mfcmapi (en) использует метод **IMAPIProp::CopyTo** для копирования свойств из MSG-файл на объект [IMAPIMessageSite](imapimessagesiteiunknown.md) .  <br/> |
|FolderDlg.cpp  <br/> |CFolderDlg::HandlePaste  <br/> |Mfcmapi (en) использует метод **IMAPIProp::CopyTo** для копирования сообщений конечного свойства из исходного сообщения во время операции вставки.  <br/> |
   
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
