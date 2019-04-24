---
title: Каноническое свойство PidTagProfileServerVersion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5d41a536-81ff-733c-2fd7-460798e057c8
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 84ff229e9914ec9074d61023873279b110fb606a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32286568"
---
# <a name="pidtagprofileserverversion-canonical-property"></a>Каноническое свойство PidTagProfileServerVersion

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Указывает сведения о версии Microsoft Exchange Server, к которой подключены учетные записи в профиле Microsoft Outlook.
  
## 

|||
|:-----|:-----|
|Связанные свойства:  <br/> |ПР_ПРОФИЛЕ_СЕРВЕР_ВЕРСИОН  <br/> |
|Идентификатор:  <br/> |0x661B  <br/> |
|Тип свойства:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Конфигурация профиля MAPI  <br/> |
   
## <a name="remarks"></a>Замечания

Профиль может указывать одну или несколько учетных записей, которые подключаются к серверу Exchange Server, но должны быть подключены к одному и тому же серверу Exchange Server.
  
Более ранние версии Outlook, чем Microsoft Office Outlook 2007, могут выполнять запись в это свойство для хранения сведений о версии сервера Exchange Server, к которой подключен активный профиль. Тем не менее формат сведений о версии различается для разных версий Exchange Server. Например, Outlook хранит в **пр_профиле_сервер_версион** десятичное значение 6944 для обозначения только номера основной сборки в идентификаторе версии **6.5.6944.3** для Microsoft Exchange Server 2003. Для подключения к Exchange 2007 Outlook хранит основной номер версии и номер основной сборки в виде сцепленного шестнадцатеричного представления этих чисел в свойстве. Идентификатор версии **8.0.685.24** для Exchange 2007 имеет основной номер версии 8 и старший номер сборки 685 в десятичном формате. При преобразовании обоих чисел в шестнадцатеричные вы получаете 0x8 и 0x2AD. Если объединить эти два числа, Outlook сохраняет значение 0x82AD в **пр_профиле_сервер_версион** в шестнадцатеричном представлении. 
  
Outlook 2007 не выполняет чтение или запись этого свойства. Он поддерживает **[пр_профиле_сервер_фулл_версион](pidtagprofileserverfullversion-canonical-property.md)**. 
  
В профиле может существовать только один из **пр_профиле_сервер_версион** или **пр_профиле_сервер_фулл_версион** , но нет гарантии, что они всегда находятся в профиле. Outlook не выполняет запись в одно свойство, пока оно не будет успешно подключено к серверу Exchange Server. 
  
В объектной модели Outlook можно использовать свойство **ексчанжемаилбокссерверверсион** объекта **Namespace** , чтобы найти версию сервера Exchange Server, на котором размещается активный почтовый ящик. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Задает определения свойств.
    
### <a name="header-files"></a>Файлы заГоловков

MAPIDEFS. h
  
> Содержит определения типов данных.
    
Мапитагс. h
  
> Содержит определения свойств, перечисленных как альтернативные имена.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойство MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

