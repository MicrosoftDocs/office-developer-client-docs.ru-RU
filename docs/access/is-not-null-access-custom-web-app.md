---
title: НЕ [] значение NULL (приложение настраиваемых web Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b941a0c7-9753-4920-bb6d-cbba94ba9422
description: Определяет, является ли указанный элемент expression равен NULL.
ms.openlocfilehash: fcbceb1e8edac65fe232ba9c2b12195b99db9545
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806960"
---
# <a name="is-not-null-access-custom-web-app"></a>НЕ [] значение NULL (приложение настраиваемых web Access)

Определяет, является ли указанный элемент expression равен NULL.
  
> [!IMPORTANT]
> Корпорация Майкрософт рекомендует больше не Создание и использование веб-приложениях Access в SharePoint. Кроме того рекомендуется использовать [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) для построения без написания кода бизнес-решений для мобильных устройств и веб. 
  
## <a name="syntax"></a>Синтаксис

 *выражение* **IS** [ *Не* ] **Значение NULL**
  
**IS [NOT] NULL** предикат содержит следующие аргументы. 
  
|||
|:-----|:-----|
| *expression*  <br/> |Любое допустимое выражение.  <br/> |
| *NOT*  <br/> |Указывает, должен быть инвертирован логическое значение. Предикат отменяет его возвращаемых значений, возвращает значение TRUE, если значение не NULL и FALSE, если значение равно NULL.  <br/> |
   
## <a name="remarks"></a>Замечания

Если значение *выражения* имеет значение NULL, ИМЕЕТ значение NULL возвращает значение TRUE; в противном случае возвращает значение FALSE. 
  
Если значение выражения имеет значение NULL, IS NOT NULL возвращает FALSE. в противном случае возвращается значение TRUE.
  

