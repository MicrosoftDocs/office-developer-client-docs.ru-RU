---
title: DTPAGE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTPAGE
api_type:
- COM
ms.assetid: 500f60ed-fdec-4d70-8cf5-664c46643956
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: a187245b2594282bc9908b3075852440f418af2b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808383"
---
# <a name="dtpage"></a>DTPAGE

  
  
**Относится к**: Outlook 
  
Описание диалогового окна, построенного из отображения таблицы с помощью функции [BuildDisplayTable](builddisplaytable.md) . 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct DTPAGE
{
  ULONG cctl;
  LPSTR lpszResourceName;
  union
  {
    LPSTR lpszComponent;
    ULONG ulItemID;
  }
  LPDTCTL lpctl;
} DTPAGE, FAR *LPDTPAGE;

```

## <a name="members"></a>Members

 **cctl**
  
> Количество элементов управления, на который указывает член **lpctl** . 
    
 **lpszResourceName**
  
> Указатель на имя или целое число идентификатор ресурс диалогового окна. 
    
 **lpszComponent**
  
> Указатель на строку, которая отображается в разделе **[Help File Mappings]** в MAPISVC.INF. Поскольку **lpszComponent** объединение с элементом **ulItemID** , только один из этих элементов содержит допустимых данных. 
    
 **ulItemID**
  
> Целочисленный идентификатор ресурса со значением меньше или равно 65535, из которой могут читать имя файла справки. Поскольку **ulItemID** объединение с элементом **lpszComponent** , только один из этих элементов содержит допустимых данных. 
    
 **lpctl**
  
> Указатель на массив структур [DTCTL](dtctl.md) , по одному для каждого элемента управления на странице. 
    
## <a name="remarks"></a>Замечания

Чтобы определить файл справки для вкладки, установите член **lpszComponent** жестко строку или член **ulItemID** для целочисленный идентификатор ресурса. 
  
Каждая запись в разделе **[Help File Mappings]** в файл Mapisvc.inf. INF состоит из строки компонента, не более 30 знаков, в левой части и путь к файлу справки в правом. **UlItemID** и **lpszResourceName** находятся в параметре _hInstance_ **BuildDisplayTable**. Для получения дополнительных сведений см [файл Mapisvc.inf. Раздел [сопоставлению файлов справки] INF](mapisvc-inf-help-file-mappings-section.md).
  
Несмотря на то, что **BuildDisplayTable** использует эту структуру для построения в таблице отображения из элемента управления ресурсами, структура **DTPAGE** никогда не отображается в самой таблицы отображения. 
  
Общие сведения о таблицах отображения разделе [Отображение таблиц](display-tables.md). Сведения о том, как реализовать отображения таблицу [Таблица отображения](display-table-implementation.md)см.
  
## <a name="see-also"></a>См. также



[BuildDisplayTable](builddisplaytable.md)
  
[DTBLPAGE](dtblpage.md)
  
[DTCTL](dtctl.md)


[Структуры MAPI](mapi-structures.md)

