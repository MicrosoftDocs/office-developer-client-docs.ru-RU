---
title: Реализация интерфейса IUnknown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 01bba63b-a2a1-490e-8b78-5c9ba8d9547b
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 5165476ea131e40153191e8625af5ea3c49f47b1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310047"
---
# <a name="implementing-the-iunknown-interface"></a>Реализация интерфейса IUnknown

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Методы интерфейса [IUnknown,](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) реализованные в каждом объекте MAPI, поддерживают межобъективную связь и управление объектами. 
  
 **IUnknown** имеет три метода: [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx), [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx)и [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx). **QueryInterface** позволяет одному объекту определить, поддерживает ли другой объект определенный интерфейс. С **Помощью QueryInterface** могут взаимодействовать два объекта без предварительного знания функциональности друг друга. Если объект, реализующий **QueryInterface,** поддерживает данный интерфейс, он возвращает указатель на реализацию интерфейса. Если объект не поддерживает запрашиваемой интерфейс, он возвращает MAPI_E_INTERFACE_NOT_SUPPORTED. 
  
Когда **RequestInterface** возвращает запрашиваемую указатель интерфейса, он также должен увеличить число ссылок нового объекта. Число ссылок объекта — это числовая величина, используемая для управления продолжительности жизни объекта. Если количество ссылок превышает 1, память объекта не может быть освобождена, так как она активно используется. Только когда количество ссылок падает до 0, объект можно безопасно освободить. 
  
Два других **метода IUnknown,** **AddRef** и **Release,** управляют количеством ссылок. **AddRef** добавляет количество ссылок, в то время как **Release** его приумношает. Все методы или функции API, возвращающих указатели интерфейса, такие как **QueryInterface,** должны вызывать **AddRef,** чтобы прибавить количество ссылок. Все реализации методов, которые получают указатели интерфейса, должны вызывать **Release,** чтобы отпустить количество, когда указатель больше не нужен. **Отпустите** проверки существующего эталонного счета, освободив память, связанную с интерфейсом, только если количество 0. 
  
> [!NOTE]
> Поскольку **addRef** и **Release** не требуются для возврата точных значений, вызыватели этих методов не должны использовать значения возврата, чтобы определить, является ли объект по-прежнему допустимым или был уничтожен. 
  
## <a name="see-also"></a>См. также



[Реализация объектов MAPI](implementing-mapi-objects.md)

