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
ms.openlocfilehash: ad8aec8d015849965bea6ac011c8a45e75c69ca1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408224"
---
# <a name="dtpage"></a>DTPAGE

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Описывает диалоговое окно, построенное из таблицы отображения [функцией BuildDisplayTable.](builddisplaytable.md) 
  
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

## <a name="members"></a>"Участники"

 **cctl**
  
> Количество элементов управления, на которые указывает **элемент lpctl.** 
    
 **lpszResourceName**
  
> Указатель на имя или идентификатор integer для ресурса диалоговых полей. 
    
 **lpszComponent**
  
> Указатель на строку, которая отображается в **разделе [Сопоставления** файлов справки] в MAPISVC.INF. Так **как lpszComponent** находится в союзе с **членом ulItemID,** только один из этих членов имеет допустимые данные. 
    
 **ulItemID**
  
> Идентификатор ресурса integer со значением меньше или равно 65535, из которого можно прочитать имя файла Справки. Так как **ulItemID** находится в союзе с **членом lpszComponent,** только один из этих членов имеет допустимые данные. 
    
 **lpctl**
  
> Указатель на массив структур [DTCTL,](dtctl.md) по одному для каждого управления на странице. 
    
## <a name="remarks"></a>Примечания

Чтобы определить файл справки для страницы вкладки, установите либо член **lpszComponent** в строку с жесткой кодом, либо **член ulItemID** к идентификатору ресурсов в составе. 
  
Каждая запись в **разделе [Сопоставления файлов справки]** в MAPISVC. INF состоит из строки компонентов, не более 30 символов, с левой стороны и пути файла справки справа. Оба **параметра ulItemID** и **lpszResourceName** находятся в  _параметре hInstance_ **BuildDisplayTable**. Дополнительные сведения см. [в mapISVC. Раздел INF [Справка сопоставления файлов]](mapisvc-inf-help-file-mappings-section.md).
  
Хотя **BuildDisplayTable** использует эту структуру для построения таблицы отображения из ресурсов управления, структура **DTPAGE** никогда не отображается в самой таблице отображения. 
  
Обзор таблиц отображения см. в таблице [Display Tables.](display-tables.md) Сведения о реализации таблицы отображения см. в таблице [Implementing a Display Table.](display-table-implementation.md)
  
## <a name="see-also"></a>См. также



[BuildDisplayTable](builddisplaytable.md)
  
[DTBLPAGE](dtblpage.md)
  
[DTCTL](dtctl.md)


[Структуры MAPI](mapi-structures.md)

