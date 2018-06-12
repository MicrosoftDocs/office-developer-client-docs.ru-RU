---
title: Каноническое свойство PidLidDistributionListMembers
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidDistributionListMembers
api_type:
- COM
ms.assetid: 029767ab-de72-4402-9cc3-31b006591042
description: '���� ���������� ���������: 9 ����� 2015 �.'
ms.openlocfilehash: c27513474048e9805bc29116aa094bc47f8f0cae
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810248"
---
# <a name="pidliddistributionlistmembers-canonical-property"></a>Каноническое свойство PidLidDistributionListMembers

  
  
**Применимо к**: Outlook 
  
Задает список EntryIds объектов, которые соответствуют членов списка рассылки.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |dispidDLMembers  <br/> |
|Набор свойств:  <br/> |PSETID_Address  <br/> |
|Длинный идентификатор (КРЫШКА):  <br/> |0x00008055  <br/> |
|Тип данных:  <br/> |PT_MV_BINARY  <br/> |
|Области:  <br/> |Контакт  <br/> |
   
## <a name="remarks"></a>Замечания

Члены списка рассылки может быть другие списки рассылки, содержащихся в контакт, пользователи глобального списка адресов или списки рассылки или адреса электронной почты одноразовых электронных адресов. Формат каждого EntryId должен быть одноразовых EntryId, как указано в [[MS-OXCDATA]](http://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx) или оболочку EntryId. 
  
Если для свойства, клиент или сервер необходимо убедиться, что его общий размер составляет менее 15 000 байт.
  
Это свойство определяет список единичных записей, соответствующих членов списка рассылки. Эти единичных записей инкапсулируют отображаемые имена и адреса электронной почты из личного списка рассылки.
  
Если этому свойству присвоено клиент или сервер, его необходимо синхронизировать с этой свойство **dispidDLMembers** для каждой записи в свойстве **dispidDLOneOffMembers** ([PidLidDistributionListOneOffMembers](pidliddistributionlistoneoffmembers-canonical-property.md)), должна быть запись в же позиции в **dispidDLOneOffMembers**.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.
    
[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> Задает свойства и операции, допустимые для контакты и списки рассылки.
    
### <a name="header-files"></a>Файлы заголовков

Mapidefs.h
  
> Содержит определения типов данных.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойства MAPI](mapi-canonical-properties.md)
  
[Каноническое свойство имена сопоставляемых именам MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI имена каноническое свойств](mapping-mapi-names-to-canonical-property-names.md)

