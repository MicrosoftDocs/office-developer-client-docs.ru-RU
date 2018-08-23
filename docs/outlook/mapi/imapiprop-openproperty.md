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
ms.openlocfilehash: e5f35474910f2257e18bcdc3b6b1dc661e2dc63a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563977"
---
# <a name="imapipropopenproperty"></a>IMAPIProp::OpenProperty

**Применимо к**: Outlook 2013 | Outlook 2016 
  
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
  
> [in] Тег свойства для свойства, которое должно осуществляться. Идентификатор и типом должны быть включены в тег свойства.
    
 _lpiid_
  
> [in] Указатель на идентификатор для интерфейса, которые будут использоваться для доступа к свойству. Параметр _lpiid_ не должно быть **значение null**.
    
 _ulInterfaceOptions_
  
> [in] Данные, связанные с интерфейсом, определенного параметром _lpiid_ . 
    
 _ulFlags_
  
> [in] Битовая маска, элементы управления доступом к свойству флагов. Можно задать следующие флажки:
    
MAPI_CREATE 
  
> Если свойство не существует, он должен быть создан. Если свойство существует, следует ли удалить текущее значение свойства. Если вызывающий объект задает флаг MAPI_CREATE, он должен установить флаг MAPI_MODIFY.
    
MAPI_DEFERRED_ERRORS 
  
> Разрешает **OpenProperty** для возврата успешно, возможно перед объект полностью доступен для вызывающего абонента. Если объект недоступен, вызов последующих объектов может вызвать ошибку. 
    
MAPI_MODIFY 
  
> MAPI_MODIFY требуется в следующих ситуациях:
    
  - При открытии свойство потока, такие как **IID_IStream**, чтобы изменить его.
    
  - При открытии вложения внедренных сообщений, такие как [PR_ATTACH_DATA_OBJ](pidtagattachdataobject-canonical-property.md) , открытый с **IID_IMessage**, чтобы изменить его.
    
 _lppUnk_
  
> [out] Указатель на запрашиваемый интерфейс, используемый для доступа к свойству.
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> Указатель запрошенного интерфейса успешно возвращен.
    
MAPI_E_INTERFACE_NOT_SUPPORTED 
  
> Запрошенный интерфейс не поддерживается для этого свойства.
    
MAPI_E_NO_ACCESS 
  
> Вызывающий не имеет разрешений на доступ к свойству.
    
MAPI_E_NO_SUPPORT 
  
> Объект не может предоставить доступ к этому свойству через интерфейс.
    
MAPI_E_NOT_FOUND 
  
> Свойство не существует и MAPI_CREATE не было задано с помощью параметра _ulFlags_ . 
    
MAPI_E_INVALID_PARAMETER 
  
> Тип свойства в теге задано значение PT_UNSPECIFIED.
    
## <a name="remarks"></a>Замечания

Метод **IMAPIProp::OpenProperty** предоставляет доступ к свойству через определенный интерфейс. **OpenProperty** является альтернативой методы [IMAPIProp::GetProps](imapiprop-getprops.md) и [IMAPIProp::SetProps](imapiprop-setprops.md) . Когда **GetProps** или **SetProps** не удается выполнить из-за слишком большой или слишком сложный вызов **OpenProperty**свойство. **OpenProperty** обычно используется для доступа к свойствам типа PT_OBJECT. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Для доступа к вложений сообщений, откройте свойства **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) с идентификатором другой интерфейс, в зависимости от типа вложения. В следующей таблице описываются вызов **OpenProperty** для разных типов вложений: 
  
|**Тип вложения**|**Идентификатор для использования интерфейса**|
|:-----|:-----|
|Двоичный  <br/> |IID_IStream  <br/> |
|String  <br/> |IID_IStream  <br/> |
|Message  <br/> |IID_IMessage  <br/> |
|OLE 2.0 (EN)  <br/> |IID_IStreamDocfile  <br/> |
   
**IStreamDocfile** является производным от интерфейса [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx) , основанный на составным файлом OLE 2.0. **IStreamDocfile** — это лучший вариант для доступа к OLE 2.0 вложения, так как он содержит меньше всего накладные расходы. IID_IStreamDocFile можно использовать для свойств, которые содержат данные, хранящиеся в структурированного хранилища, доступные через интерфейс [IStorage](http://msdn.microsoft.com/en-us/library/aa380015%28VS.85%29.aspx) . 
  
Дополнительные сведения об использовании **OpenProperty** с вложениями можно свойство **PR_ATTACH_DATA_OBJ** и [открытие вложений](opening-an-attachment.md).
  
Не используйте указатель **IStream** , который вы получаете для вызова метода его [Seek](http://msdn.microsoft.com/en-us/library/aa380043%28v=VS.85%29.aspx) или [SetSize](http://msdn.microsoft.com/en-us/library/aa380044%28v=VS.85%29.aspx) , если вы не используете ноль положение или размер переменной. Кроме того не полагайтесь на значение параметра _plibNewPosition_ выходные данные, возвращенные вызова **Seek** . 
  
При вызове **OpenProperty** для доступа к свойству с помощью интерфейса **IStream** используйте только этот интерфейс для внесения изменений. Не следует обновить свойство с любыми из другой [IMAPIProp: IUnknown](imapipropiunknown.md) методы, такие как **SetProps** или [IMAPIProp::DeleteProps](imapiprop-deleteprops.md). 
  
Не пытайтесь открыть свойство с **OpenProperty** более одного раза. Результаты, значение undefined, так как они может меняться в зависимости от поставщика для поставщика. 
  
Если требуется изменить свойства, которое должно быть открыт, необходимо задайте флаг MAPI_MODIFY. Если вы не уверены, поддерживает ли объект свойства, но вы думаете, что оно должно, необходимо задайте флаги MAPI_CREATE и MAPI_MODIFY. При использовании MAPI_CREATE, необходимо также установить MAPI_MODIFY.
  
Вы несете ответственность за преобразование указатель интерфейса, возвращаемых в параметре _lppUnk_ , которая подходит для интерфейса, указанного в параметре _lpiid_ . Возвращенный указатель необходимо также использовать для вызова метода [функции IUnknown::Release](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx) после завершения с ним. 
  
В некоторых случаях установки флагов с помощью параметра _ulFlags_ не достаточно указать тип доступа к свойству, которое является обязательным. Дополнительные данные, такие как флаги, можно размещать в параметре _ulInterfaceOptions_ . Эти данные — интерфейс зависимые. Некоторые интерфейсы (например, **IStream**) используйте его, а некоторые — нет. Например при открытии свойство так, чтобы изменить с помощью **IStream**, задайте флаг STGM_WRITE с помощью параметра _ulInterfaceOptions_ в дополнение к MAPI_MODIFY. При открытии таблицы с помощью интерфейса [IMAPITable](imapitableiunknown.md) можно включить _ulInterfaceOptions_ MAPI_UNICODE, чтобы указать, следует ли столбцы в таблице, в которых содержатся свойства строки в формате Юникод. 
  
## <a name="mfcmapi-reference"></a>Справочник по mfcmapi (en)

������ ���� mfcmapi (en) ���������� � ������� ����.
  
|**����**|**�������**|**�����������**|
|:-----|:-----|:-----|
|StreamEditor.cpp  <br/> |CStreamEditor::ReadTextStreamFromProperty  <br/> |Mfcmapi (en) используется метод **IMAPIProp::OpenProperty** для получения интерфейс потока для крупных текст и свойства двоичных файлов.  <br/> |
   
## <a name="see-also"></a>См. также

- [HrIStorageFromStream](hristoragefromstream.md) 
- [IMAPIProp::DeleteProps](imapiprop-deleteprops.md) 
- [IMAPIProp::GetProps](imapiprop-getprops.md)
- [IMAPIProp::SetProps](imapiprop-setprops.md)
- [IMAPISupport::IStorageFromStream](imapisupport-istoragefromstream.md)
- [IMAPITable : IUnknown](imapitableiunknown.md)
- [IMAPIProp : IUnknown](imapipropiunknown.md)
- [Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)
- [Открытие вложения](opening-an-attachment.md)

