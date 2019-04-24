---
title: MNLS_CompareStringW
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f8d0b7b9-2798-4d29-99e4-17da99039361
description: 'Дата последнего изменения: 20 февраля 2012 г.'
ms.openlocfilehash: dbb18ce712d7900106f2c8dd18404e47d8bdbdb7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356849"
---
# <a name="mnlscomparestringw"></a>MNLS_CompareStringW

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Сравнивает две строки Юникода.
  
```cpp
int MNLS_CompareStringW (
  LCID lcid,
  DWORD dwFlags,
  LPCWSTR pstr1,
  int cch1,
  LPCWSTR pstr2,
  int cch2);
```

## <a name="parameters"></a>Параметры

 _lcid_
  
> возврата Идентификатор языкового стандарта. Подробные сведения об определениях приведены в параметре _locale языка_ [CompareString](https://msdn.microsoft.com/library/dd317759%28VS.85%29.aspx).
    
 _dwFlags_
  
> возврата Флаги для игнорирования регистра и диакритических знаков. Подробные определения приведены в параметре _Двкмпфлагс_ [компарестринжекс](https://msdn.microsoft.com/library/dd317761%28VS.85%29.aspx).
    
 _pstr1_
  
> возврата Указатель на первую строку Юникода для сравнения.
    
 _cch1_
  
> возврата Длина в символах первой строки Юникода за исключением завершающего знака null. Приложение может предоставить отрицательное значение, если строка завершается нулем. В этом случае функция **мнлс_компарестрингв** определяет длину автоматически. 
    
 _pstr2_
  
> возврата Указатель на вторую строку Юникода для сравнения.
    
 _cch2_
  
> возврата Длина в символах второй строки Юникода, за исключением завершающего знака null. Приложение может предоставить отрицательное значение, если строка завершается нулем. В этом случае функция определяет длину автоматически.
    
## <a name="return-value"></a>Возвращаемое значение

Возвращает значения, описанные для [компарестринжекс](https://msdn.microsoft.com/library/dd317761%28VS.85%29.aspx).
  
## <a name="remarks"></a>Примечания

Эта функция служит оболочкой для [компарестрингв](https://msdn.microsoft.com/library/dd317759%28VS.85%29.aspx). **Мнлс_компарестрингв** имеет те же параметры и имеет такое же поведение, как и [компарестрингв](https://msdn.microsoft.com/library/dd317759%28VS.85%29.aspx).
  
## <a name="see-also"></a>См. также



[Компарестрингв](https://msdn.microsoft.com/library/dd317759%28VS.85%29.aspx)
  
[Компарестринжекс](https://msdn.microsoft.com/library/dd317761%28VS.85%29.aspx)

