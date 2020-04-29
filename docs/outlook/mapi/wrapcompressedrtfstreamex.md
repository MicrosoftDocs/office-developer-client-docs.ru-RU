---
title: WrapCompressedRTFStreamEx
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 45abee1c-d7fb-b0f9-522d-8ba34caf1094
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: af176c0ce327e6498a5d07f6d902c50f7323f813
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32325776"
---
# <a name="wrapcompressedrtfstreamex"></a>WrapCompressedRTFStreamEx

**Относится к**: Outlook 2013 | Outlook 2016 
  
Распаковывает текст сообщения электронной почты, который находится в формате RTF, указывает формат распакованного потока, при необходимости преобразует Распакованный поток в исходный формат и возвращает либо Распакованный поток, либо преобразованный машинный поток.
  
## <a name="quick-info"></a>Краткие сведения

|||
|:-----|:-----|
|Экспортировано:  <br/> |MSMapi32. dll  <br/> |
|Вызывающая сторона:  <br/> |Client  <br/> |
|Реализовано в:  <br/> |Outlook  <br/> |
   
```cpp
HRESULT __stdcall WrapCompressedRTFStreamEx( 
    LPSTREAM            lpCompressedRTFStream, 
    CONST RTF_WCSINFO   *pWCSInfo, 
    LPSTREAM            *lppUncompressedRTFStream, 
    RTF_WCSRETINFO      *pRetInfo); 

```

## <a name="parameters"></a>Параметры

_лпкомпресседртфстреам_
  
> возврата Это указатель на поток, Открытый на [каноническое свойство PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md) сообщения. 
    
_пвксинфо_
  
> возврата Это указатель на 
    
   Структура [RTF_WCSINFO](rtf_wcsinfo.md) , содержащая параметры функции. 
    
_лппункомпресседртфстреам_
  
> вышли Это указатель на расположение, в котором возвращается поток для распакованного RTF. 
    
_претинфо_
  
> вышли Это указатель на структуру [RTF_WCSRETINFO](rtf_wcsretinfo.md) , которая содержит сведения о формате возвращенного распакованного потока. 
    
## <a name="return-values"></a>Возвращаемые значения

S_OK 
  
- Вызов функции выполнен успешно.
    
MAPI_E_INVALID_PARAMETER 
  
- Это возвращается в том случае, если флаг **MAPI_NATIVE_BODY** объединен с флагом **MAPI_MODIFY** в поле **ulFlags** структуры **RTF_WCSINFO** , на которую указывает *пвксинфо* . 
    
## <a name="remarks"></a>Примечания

**Врапкомпресседртфстреамекс** позволяет получить доступ к тексту сообщения электронной почты, инкапсулированного в сжатом формате RTF, путем распаковки потока, возвращения распакованного потока и его формата, а также собственного потока основного текста. Собственный поток основного текста может быть в формате RTF, обычного текста или HTML. 
  
Объектная модель Microsoft Office Outlook предоставляет свойство **Body** для объектов **MailItem** и [свойство MailItem. BodyFormat (Outlook)](https://msdn.microsoft.com/library/f635a0bc-20b7-206c-f558-a4ca2519670f%28Office.15%29.aspx) , которое указывает формат основного текста. При проектировании решение, не пользующееся доверием Outlook, вызывает диалоговые окна безопасности, созданные в Outlook Security Guard. Использование экспортированной функции MAPI **врапкомпресседртфстреамекс** позволяет решению использовать MAPI вместо объектной модели Outlook и избегать использования диалоговых окон безопасности. 
  
Так как **флаг\_NATIVE_BODY MAPI** не может сочетаться с флагом **изменения\_MAPI** в поле **ulFlags** структуры **RTF\_вксинфо** , на которую указывает *пвксинфо*, можно получить доступ только к исходному потоку основного текста в режиме только для чтения. Чтобы получить доступ к основному потоку основного текста в режиме чтения и записи, следует использовать функцию **врапкомпресседртфстреам** . 
  
## <a name="see-also"></a>См. также

- [Получение текста сообщения в сжатом формате RTF и его преобразование в исходный формат](how-to-retrieve-the-body-of-a-message-in-compressed-rtf-and-convert.md)

