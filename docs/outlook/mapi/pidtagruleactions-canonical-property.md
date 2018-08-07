---
title: Каноническое свойство PidTagRuleActions
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRuleActions
api_type:
- COM
ms.assetid: 3ec4259a-8fe9-46c3-82b8-42c6907b8515
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 6edebdb63a63b9df830ae549c0f0d9146f6eb82e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811765"
---
# <a name="pidtagruleactions-canonical-property"></a>Каноническое свойство PidTagRuleActions

  
  
**Относится к**: Outlook 
  
Содержит набор действия, связанные с правилом. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_RULE_ACTIONS  <br/> |
|Идентификатор:  <br/> |0x6680  <br/> |
|Тип данных:  <br/> |PT_ACTIONS  <br/> |
|Область:  <br/> |Правила со стороны сервера  <br/> |
   
## <a name="remarks"></a>Замечания

Действия выражаются в действие правила и буфера значение свойства содержит структуру правила действие данные буфера упакованы как указано в [[MS-OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx).
  
## <a name="mfcmapi-reference"></a>Справочник по mfcmapi (en)

������ ���� mfcmapi (en) ���������� � ������� ����.
  
|**����**|**�������**|**�����������**|
|:-----|:-----|:-----|
|ImportProcs.cpp  <br/> |PropCopyMore HrCopyActions  <br/> |Эти функции демонстрируют анализа свойства PT_ACTIONS в целях копирования еще одно свойство.  <br/> |
   
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные спецификаций протокола Exchange Server.
    
[[MS-OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)
  
> Управляет входящие сообщения электронной почты на сервере.
    
### <a name="header-files"></a>Файлы заголовков

Mapidefs.h
  
> Содержит определения типов данных.
    
Mapitags.h
  
> Содержит определения свойства в списке альтернативных имен.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

