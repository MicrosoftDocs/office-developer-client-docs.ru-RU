---
title: ShowOptions
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 51acac58-ec39-488f-979c-1887dc2ab94b
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 5b58b71dc4f2441448eb3e0dac2c3c5763675927
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407699"
---
# <a name="showoptions"></a>ShowOptions

**Область применения:** Excel 2013 | Office 2013 | Visual Studio 
  
Отображает модальные диалоговые окна для сбора сведений от пользователя. Эта точка входа вызвана, когда пользователь нажимает кнопку "Параметры" рядом с полем типа кластера  для выбранного  соединитела кластера в диалоговом окне "Параметры **Excel"** (в категории "Дополнительные" в разделе "Формулы").   Соединители кластера отвечают за реализацию собственного диалогового интерфейса параметров и хранение связанных данных в реестре или другом месте. Параметры являются внутренними для соединители кластера. Excel не знает о них. 
  
```cpp
int ShowOptions(HWND hWndParent)
```

## <a name="parameters"></a>Параметры

_hWndParent_
  
> Окне Excel.
    
## <a name="return-value"></a>Возвращаемое значение

**xlHpcRetSuccess,** если было показано диалоговое окно; **xlHpcRetCallFailed,** если он не был показан. 
  
## <a name="remarks"></a>Примечания

Соединители кластера могут использовать это диалоговое окно для получения сведений, например о том, какой сервер кластера использовать, от пользователя.
  
## <a name="see-also"></a>См. также

- [Функции для работы с соединителями кластеров Excel](excel-cluster-connector-functions.md)

