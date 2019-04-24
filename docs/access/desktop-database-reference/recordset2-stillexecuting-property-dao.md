---
title: Свойство Recordset2. Стиллексекутинг (DAO)
TOCTitle: StillExecuting Property
ms:assetid: f051c350-0451-44fe-0e47-b152bae4b481
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836546(v=office.15)
ms:contentKeyID: 48548601
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: aa94622374990ce48c857e9ad45c3531975bb9a8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307219"
---
# <a name="recordset2stillexecuting-property-dao"></a>Свойство Recordset2. Стиллексекутинг (DAO)


**Область применения**: Access 2013, Office 2013

## <a name="syntax"></a>Синтаксис

*Expression* . Стиллексекутинг

*Expression (выражение* ) Переменная, представляющая объект **Recordset2** .

## <a name="remarks"></a>Замечания

Используйте свойство **стиллексекутинг** , чтобы определить, завершен ли последний вызов метода асинхронного **выполнения** или **OpenConnection** (то есть метод, выполняемый с параметром **дбрунасинк** ). Несмотря на то, что свойство **стиллексекутинг** имеет **значение true**, доступ к возвращенному объекту невозможен.

После того как свойство **стиллексекутинг** возвращает **значение false**, после вызова **OpenConnection** , возвращающего связанный объект **Connection** , можно ссылаться на объект. До тех пор пока **стиллексекутинг** остается **true**, на объект не может быть ссылок, кроме чтения свойства **стиллексекутинг** .

Используйте метод **[Cancel](connection-cancel-method-dao.md)** , чтобы прекратить выполнение задачи в ходе выполнения.

