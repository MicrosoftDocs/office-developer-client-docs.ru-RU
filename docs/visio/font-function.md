---
title: Функция FONT
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 20b587ee-87bf-4648-99ec-ddedd703d9fd
description: Возвращает целое значение уникальный идентификатор для шрифта, указанный в параметре name.
ms.openlocfilehash: 4afd2aa05f2103675bf0df8db5cc7ea21f45fe71
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813804"
---
# <a name="font-function"></a>Функция FONT

Возвращает целое значение уникальный идентификатор для шрифта, указанный в параметре name.
  
> [!NOTE]
> В большинстве случаев идентификатор шрифта относящиеся к системе. Хотя шрифта остается установленным один раз используется в файле, функция **ШРИФТА** предоставляет согласованный доступ для определенного шрифта в системах и версий Visio. Рекомендуется использовать функцию **ШРИФТА** для назначения шрифты вместо непосредственно идентификаторы шрифта. 
  
## <a name="version-information"></a>Сведения о версии

Добавлена версия: Visio 2013
 
  
## <a name="syntax"></a>Синтаксис

 **ШРИФТ** ( _«font_name_string»_)
  
### <a name="parameters"></a>Параметры

|**Имя**|**Обязательный или необязательный**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _font_name_string_ <br/> |Обязательный  <br/> |**string** <br/> |Имя шрифта.  <br/> |
   
## <a name="return-value"></a>������������ ��������

Целое число
  
## <a name="remarks"></a>Замечания

Если строка для *font_name_string* не соответствует известной шрифта, эта функция возвращает #VALUE! Ошибка. 
  
## <a name="example"></a>Пример

 `FONT("Calibri")`
  
Возвращает целое значение, представляющее уникальный идентификатор для шрифта «Calibri» (4).
  

