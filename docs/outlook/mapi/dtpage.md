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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Описывает диалоговое окно, построенное из отображаемой таблицы [функцией BuildDisplayTable.](builddisplaytable.md) 
  
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
  
> Указатель на имя или идентификатор для ресурса диалоговых окно. 
    
 **lpszComponent**
  
> Указатель на строку, которая отображается в разделе **[Сопоставления** файлов справки] в MAPISVC.INF. Так **как lpszComponent** находится в объединение с членом **ulItemID,** только один из этих членов имеет допустимые данные. 
    
 **ulItemID**
  
> Integer resource identifier with a value less than or equal to 65535 from which the Help file name can be read. Так **как ulItemID** находится в объединение с **членом lpszComponent,** только один из этих членов имеет допустимые данные. 
    
 **lpctl**
  
> Указатель на массив структур [DTCTL,](dtctl.md) по одному для каждого управления на странице. 
    
## <a name="remarks"></a>Примечания

Чтобы определить файл справки для страницы вкладок, задайте для члена **lpszComponent** строку с жестко заданным кодом или для члена **ulItemID** — для идентификатора ресурса integer. 
  
Каждая запись в разделе **[Сопоставления файлов справки]** в MAPISVC. INF состоит из строки компонента длиной не более 30 символов с левой стороны и пути к файлу справки справа. **ulItemID** и **lpszResourceName** находятся в параметре _hInstance_ **BuildDisplayTable.** Дополнительные сведения см. в [mapISVC. INF [Help File Mappings] Section](mapisvc-inf-help-file-mappings-section.md).
  
Хотя **BuildDisplayTable** использует эту структуру для построения таблицы отображения из ресурсов управления, **структура DTPAGE** никогда не отображается в самой таблице отображения. 
  
Обзор таблиц отображения см. в [таблице отображения.](display-tables.md) Сведения о реализации таблицы отображения см. в таблице ["Реализация таблицы отображения".](display-table-implementation.md)
  
## <a name="see-also"></a>См. также



[BuildDisplayTable](builddisplaytable.md)
  
[DTBLPAGE](dtblpage.md)
  
[DTCTL](dtctl.md)


[Структуры MAPI](mapi-structures.md)

