---
title: IMAPIPropOpenProperty
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProp.OpenProperty
api_type:
- COM
ms.assetid: e400e6cc-4e36-43fc-9304-b688a0a7fd77
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 7bf1d6912e44319c36e288cd3870218e8c4e45ff
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319812"
---
# <a name="imapipropopenproperty"></a>IMAPIProp::OpenProperty

**Область применения**: Outlook 2013 | Outlook 2016 
  
Возвращает указатель в интерфейс, который можно использовать для доступа к свойству.
  
```cpp
HRESULT OpenProperty(
  ULONG ulPropTag,
  LPCIID lpiid,
  ULONG ulInterfaceOptions,
  ULONG ulFlags,
  LPUNKNOWN FAR * lppUnk
);
```

## <a name="parameters"></a>Parameters

 _ulPropTag_
  
> [in] Тег свойства для доступа к свойству. Идентификатор и тип должны быть включены в тег свойства.
    
 _lpiid_
  
> [in] Указатель на идентификатор для интерфейса, который будет использоваться для доступа к свойству. Параметр  _lpiid_ не должен быть **null**.
    
 _ulInterfaceOptions_
  
> [in] Данные, которые связаны с интерфейсом, определенным _параметром lpiid._ 
    
 _ulFlags_
  
> [in] Битмаска флагов, которые контролируют доступ к свойству. Можно установить следующие флаги:
    
MAPI_CREATE 
  
> Если свойство не существует, оно должно быть создано. Если свойство существует, текущее значение свойства должно быть отброшено. Когда вызываемая MAPI_CREATE задает флаг, он также должен MAPI_MODIFY флаг.
    
MAPI_DEFERRED_ERRORS 
  
> Позволяет **OpenProperty** успешно возвращаться, возможно, до того, как объект будет полностью доступен вызываемой. Если объект не доступен, при последующем вызове объекта может быть допущена ошибка. 
    
MAPI_MODIFY 
  
> MAPI_MODIFY в таких ситуациях:
    
  - При открытии свойства потока, например **IID_IStream,** изменить его.
    
  - При открытии встроенного вложения сообщения, например [PR_ATTACH_DATA_OBJ](pidtagattachdataobject-canonical-property.md) с **IID_IMessage,** чтобы изменить его.
    
 _lppUnk_
  
> [вышел] Указатель на запрашиваемом интерфейсе, который будет использоваться для доступа к свойству.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Запрашиваемая указка интерфейса была успешно возвращена.
    
MAPI_E_INTERFACE_NOT_SUPPORTED 
  
> Запрашиваемая поддержка интерфейса для этого свойства не поддерживается.
    
MAPI_E_NO_ACCESS 
  
> У вызываемого недостаточно разрешений на доступ к свойству.
    
MAPI_E_NO_SUPPORT 
  
> Объект не может предоставить доступ к этому свойству через запрашиваемом интерфейсе.
    
MAPI_E_NOT_FOUND 
  
> Запрашиваемая свойство не существует, MAPI_CREATE не была задана в _параметре ulFlags._ 
    
MAPI_E_INVALID_PARAMETER 
  
> Тип свойства в теге установлен для PT_UNSPECIFIED.
    
## <a name="remarks"></a>Примечания

Метод **IMAPIProp::OpenProperty** предоставляет доступ к свойству с помощью определенного интерфейса. **OpenProperty** — это альтернатива методам [IMAPIProp::GetProps](imapiprop-getprops.md) и [IMAPIProp::SetProps.](imapiprop-setprops.md) Если **getProps или** **SetProps** не удается из-за слишком большого или слишком сложного свойства, позвоните **в OpenProperty**. **OpenProperty** обычно используется для доступа к свойствам типа PT_OBJECT. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Чтобы получить доступ к **вложениям сообщений, откройте свойство PR_ATTACH_DATA_OBJ** [(PidTagAttachDataObject)](pidtagattachdataobject-canonical-property.md)с другим идентификатором интерфейса в зависимости от типа вложения. В следующей таблице описывается, как вызывать **OpenProperty** для различных типов вложений: 
  
|**Тип вложения**|**Идентификатор интерфейса для использования**|
|:-----|:-----|
|В двоичном формате  <br/> |IID_IStream  <br/> |
|String  <br/> |IID_IStream  <br/> |
|Сообщение  <br/> |IID_IMessage  <br/> |
|OLE 2.0  <br/> |IID_IStreamDocfile  <br/> |
   
**IStreamDocfile** является производным интерфейса [IStream,](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) основанного на сложном файле OLE 2.0. **IStreamDocfile** — это лучший выбор для доступа к вложениям OLE 2.0, так как он включает наименьшее количество накладных расходов. Вы можете использовать IID_IStreamDocFile для тех свойств, которые содержат данные, хранимые в структурированном хранилище, доступном с помощью [интерфейса IStorage.](https://msdn.microsoft.com/library/aa380015%28VS.85%29.aspx) 
  
Дополнительные сведения об использовании **OpenProperty** с **вложениями см.** в PR_ATTACH_DATA_OBJ свойстве [и открытии вложения.](opening-an-attachment.md)
  
Не используйте указатель **IStream,** который вы получаете, чтобы вызвать метод [Seek](https://msdn.microsoft.com/library/aa380043%28v=VS.85%29.aspx) или [SetSize,](https://msdn.microsoft.com/library/aa380044%28v=VS.85%29.aspx) если вы не используете переменную с нулевой или размерной позицией. Кроме того, не полагаться на значение параметра _вывода plibNewPosition,_ возвращаемого из вызова **Seek.** 
  
Если вы **вызываете OpenProperty** для доступа к свойству с интерфейсом **IStream,** используйте только этот интерфейс, чтобы внести в него изменения. Не пытайтесь обновить свойство с помощью других методов [IMAPIProp: IUnknown,](imapipropiunknown.md) таких как **SetProps** или [IMAPIProp::D eleteProps](imapiprop-deleteprops.md). 
  
Не пытайтесь открыть свойство с **OpenProperty** несколько раз. Результаты неопределяются, так как они могут отличаться от поставщика к поставщику. 
  
Если необходимо изменить открываемую свойство, установите MAPI_MODIFY флаг. Если вы не уверены, поддерживает ли объект свойство, но считаете, что оно должно быть, установите MAPI_CREATE и MAPI_MODIFY флаги. Всякий MAPI_CREATE установлено, MAPI_MODIFY также необходимо установить.
  
Вы несете ответственность за перенаставку указателя интерфейса, возвращаемого в _параметре lppUnk,_ на тот, который подходит для интерфейса, указанного в параметре _lpiid._ Вы также должны использовать возвращенный указатель для вызова метода [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) по его завершению. 
  
Иногда для установки флагов в параметре  _ulFlags_ недостаточно указать тип доступа к свойству, которое требуется. Дополнительные данные, например флаги, можно поместить в параметр _ulInterfaceOptions._ Эти данные зависят от интерфейса. Некоторые интерфейсы **(например, IStream)** используют его, а другие — нет. Например, при открываемом свойстве, который необходимо изменить с **помощью IStream,** установите флаг STGM_WRITE в параметре  _ulInterfaceOptions_ в дополнение к MAPI_MODIFY. При открывлении таблицы с помощью интерфейса [IMAPITable](imapitableiunknown.md) можно задать  _ulInterfaceOptions_ MAPI_UNICODE, чтобы указать, должны ли столбцы в таблице с свойствами строки быть в формате Unicode. 
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|StreamEditor.cpp  <br/> |CStreamEditor::ReadTextStreamFromProperty  <br/> |MFCMAPI использует **метод IMAPIProp::OpenProperty** для получения интерфейса потока для больших текстовых и двоичных свойств.  <br/> |
   
## <a name="see-also"></a>См. также

- [HrIStorageFromStream](hristoragefromstream.md) 
- [IMAPIProp::DeleteProps](imapiprop-deleteprops.md) 
- [IMAPIProp::GetProps](imapiprop-getprops.md)
- [IMAPIProp::SetProps](imapiprop-setprops.md)
- [IMAPISupport::IStorageFromStream](imapisupport-istoragefromstream.md)
- [IMAPITable : IUnknown](imapitableiunknown.md)
- [IMAPIProp : IUnknown](imapipropiunknown.md)
- [MFCMAPI как пример кода](mfcmapi-as-a-code-sample.md)
- [Открытие вложения](opening-an-attachment.md)

