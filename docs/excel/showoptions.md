---
title: ShowOptions
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 51acac58-ec39-488f-979c-1887dc2ab94b
description: '������� ����������: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: dbf6f0f50e9f7fa988e83f3b58012e9deac13eac
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807322"
---
# <a name="showoptions"></a>ShowOptions

**Применимо к**: Excel 2013 | Office 2013 | Visual Studio 
  
Показывает модального диалогового окна для сбора сведений у пользователя. Эта точка входа вызывается, когда пользователь нажимает кнопку **Параметры** рядом с полем **тип кластера** для соединителя выбранного кластера в диалоговом окне **Параметры Excel** (в категории **Дополнительно** в разделе **формулы** ). Соединителей кластеров отвечают для реализации интерфейса диалогового окна собственные параметры, а также для хранения связанных данных в реестре или в другом месте. Параметры являются внутренними относительно соединитель кластера. Excel не знать о них. 
  
```cpp
int ShowOptions(HWND hWndParent)
```

## <a name="parameters"></a>Parameters

_hWndParent_
  
> Дескриптор окна Excel.
    
## <a name="return-value"></a>������������ ��������

**xlHpcRetSuccess** Если было показано диалоговое окно; **xlHpcRetCallFailed** , если он не отображается. 
  
## <a name="remarks"></a>Замечания

Соединителей кластеров можно использовать это диалоговое окно для получения информации, например какие кластера-сервера, у пользователя.
  
## <a name="see-also"></a>См. также

- [Функции соединителя кластера Excel](excel-cluster-connector-functions.md)

