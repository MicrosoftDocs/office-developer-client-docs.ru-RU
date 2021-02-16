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

**Относится к**: Outlook 2013 | Outlook 2016 
  
Возвращает указатель на интерфейс, который можно использовать для доступа к свойству.
  
```cpp
HRESULT OpenProperty(
  ULONG ulPropTag,
  LPCIID lpiid,
  ULONG ulInterfaceOptions,
  ULONG ulFlags,
  LPUNKNOWN FAR * lppUnk
);
```

## <a name="parameters"></a>Параметры

 _ulPropTag_
  
> [in] Тег свойства для свойства, к нему необходимо получить доступ. Идентификатор и тип должны быть включены в тег свойства.
    
 _lpiid_
  
> [in] Указатель на идентификатор интерфейса, который будет использоваться для доступа к свойству. Параметр _lpiid_ не должен иметь **null.**
    
 _ulInterfaceOptions_
  
> [in] Данные, которые связаны с интерфейсом, определенным _параметром lpiid._ 
    
 _ulFlags_
  
> [in] Битоваяmas флагов, которая управляет доступом к свойству. Можно установить следующие флаги:
    
MAPI_CREATE 
  
> Если свойство не существует, его следует создать. Если свойство существует, текущее значение свойства должно быть удалено. Когда вызываемая вызываемая MAPI_CREATE, она также должна установить MAPI_MODIFY флага.
    
MAPI_DEFERRED_ERRORS 
  
> Позволяет **OpenProperty** успешно возвращаться, возможно, до того, как объект будет полностью доступен вызываемой. Если объект не доступен, последующий вызов объекта может вызвать ошибку. 
    
MAPI_MODIFY 
  
> MAPI_MODIFY в таких ситуациях:
    
  - При открытии свойства stream, например **IID_IStream,** чтобы изменить его.
    
  - При открытии внедренного вложения сообщения, [например](pidtagattachdataobject-canonical-property.md) PR_ATTACH_DATA_OBJ с помощью IID_IMessage, чтобы изменить его.
    
 _lppUnk_
  
> [out] Указатель на запрашиваемую интерфейс, которая будет использоваться для доступа к свойству.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Запрашиваемая указатель интерфейса успешно возвращена.
    
MAPI_E_INTERFACE_NOT_SUPPORTED 
  
> Запрашиваемая поддержка интерфейса для этого свойства не поддерживается.
    
MAPI_E_NO_ACCESS 
  
> У вызываемого объекта недостаточно разрешений на доступ к свойству.
    
MAPI_E_NO_SUPPORT 
  
> Объект не может предоставить доступ к этому свойству через запрашивается интерфейс.
    
MAPI_E_NOT_FOUND 
  
> Запрашиваемая свойство не существует, MAPI_CREATE не задана в _параметре ulFlags._ 
    
MAPI_E_INVALID_PARAMETER 
  
> Тип свойства в теге имеет PT_UNSPECIFIED.
    
## <a name="remarks"></a>Примечания

Метод **IMAPIProp::OpenProperty** предоставляет доступ к свойству через определенный интерфейс. **OpenProperty —** это альтернатива методам [IMAPIProp::GetProps](imapiprop-getprops.md) и [IMAPIProp::SetProps.](imapiprop-setprops.md) Если происходит **сбой GetProps** или **SetProps** из-за слишком большого или слишком сложного свойства, вызовите **OpenProperty.** **OpenProperty** обычно используется для доступа к свойствам типа PT_OBJECT. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Чтобы получить доступ к вложениям сообщений, откройте **свойство PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject)](pidtagattachdataobject-canonical-property.md)с другим идентификатором интерфейса в зависимости от типа вложения. В следующей таблице описывается вызов **OpenProperty** для различных типов вложений: 
  
|**Тип вложения**|**Идентификатор интерфейса для использования**|
|:-----|:-----|
|Binary  <br/> |IID_IStream  <br/> |
|String  <br/> |IID_IStream  <br/> |
|Сообщение  <br/> |IID_IMessage  <br/> |
|OLE 2.0  <br/> |IID_IStreamDocfile  <br/> |
   
**IStreamDocfile** — это производный интерфейс [IStream,](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) основанный на составном файле OLE 2.0. **IStreamDocfile** является лучшим выбором для доступа к вложениям OLE 2.0, так как он требует наименьшего объема накладных расходов. Вы можете использовать IID_IStreamDocFile для тех свойств, которые содержат данные, хранимые в структурированном хранилище, доступном через [интерфейс IStorage.](https://msdn.microsoft.com/library/aa380015%28VS.85%29.aspx) 
  
Дополнительные сведения об использовании **OpenProperty** с **вложениями** см. в свойстве PR_ATTACH_DATA_OBJ [и открытии вложения.](opening-an-attachment.md)
  
Не используйте **указатель IStream,** который вы получаете, для вызова метода [Seek](https://msdn.microsoft.com/library/aa380043%28v=VS.85%29.aspx) или [SetSize,](https://msdn.microsoft.com/library/aa380044%28v=VS.85%29.aspx) если не используется переменная нулевого положения или размера. Кроме того, не полагайтесь на значение выходного _параметра plibNewPosition,_ возвращаемого вызовом **Seek.** 
  
При вызове **OpenProperty** для доступа к свойству с помощью **интерфейса IStream** используйте только этот интерфейс для внесения изменений в него. Не пытайтесь обновить свойство с помощью других методов [IMAPIProp : IUnknown,](imapipropiunknown.md) таких как **SetProps** или [IMAPIProp::D eleteProps.](imapiprop-deleteprops.md) 
  
Не пытайтесь открыть свойство с **помощью OpenProperty** несколько раз. Результаты не задаются, так как они могут отличаться от поставщика к поставщику. 
  
Если необходимо изменить свойство для открытия, установите флаг MAPI_MODIFY. Если вы не знаете, поддерживает ли объект свойство, но считаете, что оно должно быть, установите флаги MAPI_CREATE и MAPI_MODIFY. Каждый MAPI_CREATE установлен, MAPI_MODIFY также должен быть установлен.
  
Вы несете ответственность за перенастраив указатель интерфейса, возвращенный в параметре _lppUnk,_ на тот, который подходит для интерфейса, указанного в параметре _lpiid._ Вы также должны использовать возвращенный указатель для вызова метода [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) после завершения работы с ним. 
  
Иногда установки флагов в параметре  _ulFlags_ недостаточно, чтобы указать тип доступа к свойству, которое требуется. В параметр  _ulInterfaceOptions_ можно поместить дополнительные данные, например флаги. Эти данные зависят от интерфейса. Некоторые интерфейсы **(например, IStream)** используют его, а другие — нет. Например, при открываемом свойстве, износимом с помощью **IStream,** установите флаг STGM_WRITE в параметре  _ulInterfaceOptions_ в дополнение к MAPI_MODIFY. При открытие таблицы с помощью интерфейса [IMAPITable](imapitableiunknown.md) можно установить для  _ulInterfaceOptions_ MAPI_UNICODE, чтобы указать, должны ли столбцы таблицы, в которые будут вметься свойства строки, быть в формате Юникод. 
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|StreamEditor.cpp  <br/> |CStreamEditor::ReadTextStreamFromProperty  <br/> |MFCMAPI использует метод **IMAPIProp::OpenProperty** для получения интерфейса потока для больших текстовых и двоичных свойств.  <br/> |
   
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

