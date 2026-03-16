db.productos.aggregate([{$group: {_id: "$categoria",stockTotal: { $sum: "$stock" }}},{$project: {_id: 0,categoria: "$_id",stockTotal: 1}}])

