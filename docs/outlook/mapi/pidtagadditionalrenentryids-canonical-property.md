---
title: Каноническое свойство PidTagAdditionalRenEntryIds
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAdditionalRenEntryIds
api_type:
- HeaderDef
ms.assetid: 8c6e7ca2-1824-4cca-bf69-3c1ea52727de
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: e63d661ab8c7e410d6a0dd786819cc189813017e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810799"
---
# <a name="pidtagadditionalrenentryids-canonical-property"></a>Каноническое свойство PidTagAdditionalRenEntryIds

  
  
**Относится к**: Outlook 
  
Содержит запись идентификаторы из специальных папок. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_ADDITIONAL_REN_ENTRYIDS  <br/> |
|Идентификатор:  <br/> |0x36D8  <br/> |
|Тип данных:  <br/> |PT_MV_BINARY  <br/> |
|Область:  <br/> |Приложения Outlook  <br/> |
   
## <a name="remarks"></a>Замечания

Первые пять записей этого многозначные свойства применяются к следующим папкам, если они существуют в хранилище.
  
0 — папки "конфликты"
  
1 — синхронизации папки проблемы
  
2 - папка Локальные ошибки
  
3 - папка сбои сервер
  
4 - нежелательной почты в соответствующую папку
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные спецификаций протокола Exchange Server.
    
[[MS-OXOSFLD]](http://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)
  
> Задает свойства и операции по созданию и поиск специальные папки в почтовом ящике.
    
[[MS-OXPHISH]](http://msdn.microsoft.com/library/ed49ab26-ba13-4d4c-8a94-98d4ceecd4b7%28Office.15%29.aspx)
  
> Идентифицирует и помечает сообщения электронной почты, которые предназначены для побудить получателей разглашение конфиденциальной информации (например, пароли и другие личные сведения) чтобы-надежного источника.
    
[[MS-OXCSPAM]](http://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)
  
> Включает обработку списки разрешенных и запрещенных и определение нежелательных сообщений электронной почты.
    
### <a name="header-files"></a>Файлы заголовков

Mapitags.h
  
> Содержит определения свойств указано, что связанными свойствами.
    
Mapidefs.h
  
> Содержит определения типов данных.
    
## <a name="see-also"></a>См. также



[Каноническое свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)


[Сведения об API хранилищ](http://msdn.microsoft.com/en-us/library/aa192884.aspx)

