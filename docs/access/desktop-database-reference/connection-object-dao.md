---
title: Connection Object (DAO)
TOCTitle: Connection Object
ms:assetid: f469b04e-2539-6b53-31f2-85fe22fcc2fc
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836694(v=office.15)
ms:contentKeyID: 48548690
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: bba06d593069051d2cc4f2e66b8cb91f36d920fb
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25480570"
---
# <a name="connection-object-dao"></a>Connection Object (DAO)


**Применимо к**: Access 2013 | Office 2013


> [!NOTE]
> <P>Рабочие области технология ODBCDirect не поддерживаются в Microsoft Access 2013. Использование ADO, если вы хотите получить доступ к внешним источникам данных без использования ядро базы данных Microsoft Access.</P>



Объект **подключения** представляет подключение к базе данных ODBC (только для рабочих областей технология ODBCDirect).

## <a name="remarks"></a>Замечания

**Подключение** — это непостоянные объект, представляющий подключение к удаленной базе данных. Объект **подключения** доступен только в рабочие области технология ODBCDirect (то есть, **рабочей области** объект, созданных с помощью параметра типа **dbUseODBC**).


> [!NOTE]
> <P>Код, написанный для более ранних версий DAO можно продолжить использование объекта <STRONG>базы данных</STRONG> для обеспечения обратной совместимости, но при желании новые возможности <STRONG>подключения</STRONG> , необходимо проверить код, чтобы использовать объект <STRONG>подключения</STRONG> . Чтобы упростить преобразование кода, можно получить ссылку на объект <STRONG>подключения</STRONG> из <STRONG>базы данных</STRONG> , прочитав статью свойство <A href="database-connection-property-dao.md">Connection</A> объекта <STRONG>базы данных</STRONG> . С другой стороны можно получить ссылку на объект <STRONG>базы данных</STRONG> из свойства объекта <STRONG>подключения к</STRONG> <STRONG>базе данных</STRONG> .</P>


