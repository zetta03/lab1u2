
# lab1u2

create table Recipe (id INT NOT NULL PRIMARY KEY AUTO_INCREMENT, name VARCHAR(25), description VARCHAR(50), instructions VARCHAR(500)) ENGINE=InnoDB DEFAULT CHARSET=utf8;
	

	create table Ingredient (id INT NOT NULL PRIMARY KEY AUTO_INCREMENT, name VARCHAR(50)) ENGINE=InnoDB DEFAULT CHARSET=utf8; 
	

	create table Measure (id INT NOT NULL PRIMARY KEY AUTO_INCREMENT, name VARCHAR(30)) ENGINE=InnoDB DEFAULT CHARSET=utf8; 
	

	create table RecipeIngredient (recipe_id INT NOT NULL, ingredient_id INT NOT NULL, measure_id INT, amount INT, 
	

		CONSTRAINT fk_recipe FOREIGN KEY(recipe_id) REFERENCES Recipe(id), 
	

		CONSTRAINT fk_ingredient FOREIGN KEY(ingredient_id) REFERENCES Ingredient(id), 
	

		CONSTRAINT fk_measure FOREIGN KEY(measure_id) REFERENCES Measure(id)) 
	

		ENGINE=InnoDB DEFAULT CHARSET=utf8; 
	  
	  

INSERT INTO Measure (name) VALUES('CUP'), ('TEASPOON'), ('TABLESPOON'), ('WHOLE'), ('POUNDS');


INSERT INTO Ingredient (name) VALUES('egg'), ('romaine lettuce'), ('olive oil'), ('caesar dressing'), ('salt'), ('sugar'), ('milk'), ('baking powder'), ('flour'), ('melted butter'), ('butter'), ('potatoes'), ('heavy cream'), ('sour cream');


INSERT INTO Recipe (name, description, instructions) VALUES('pancakes', 'flat cake', 'Whisk dry ingredients. Combine remaining ingredients. Heat griddle. Pour out ¼ cup of batter for each pancake. Cook about 1-2 minutes or until bubbles appear, flip cook an additional 2-3 minutes or until golden brown.');
INSERT INTO Recipe (name, description, instructions) VALUES('mashed potatoes', 'fluffy potatoes', 'Peel and rinse then cut into quarters. Bring water and potatoes to boil. Cook drain and mash.');
INSERT INTO Recipe (name, description, instructions) VALUES('caesar salad', 'leafy salad', 'Rinse and chop lettuce. Put lettuce in a bowl and drizzle with olive oil and dressing. Optional: salt and pepper to taste );

INSERT INTO RecipeIngredient (recipe_id, ingredient_id, measure_id, amount) VALUES (1, 1, 4, 1);
INSERT INTO RecipeIngredient (recipe_id, ingredient_id, measure_id, amount) VALUES (1, 2, 2, 1);
INSERT INTO RecipeIngredient (recipe_id, ingredient_id, measure_id, amount) VALUES (1, 3, 3, 1);
INSERT INTO RecipeIngredient (recipe_id, ingredient_id, measure_id, amount) VALUES (1, 4, 1, 1 );
INSERT INTO RecipeIngredient (recipe_id, ingredient_id, measure_id, amount) VALUES (1, 5, 3, 1);
INSERT INTO RecipeIngredient (recipe_id, ingredient_id, measure_id, amount) VALUES (1, 6, 1, 1 );
INSERT INTO RecipeIngredient (recipe_id, ingredient_id, measure_id, amount) VALUES (1, 7, 3, 3);

INSERT INTO RecipeIngredient (recipe_id, ingredient_id, measure_id, amount) VALUES (2, 9, 5, 5);
INSERT INTO RecipeIngredient (recipe_id, ingredient_id, measure_id, amount) VALUES (2, 8, 3, 12);
INSERT INTO RecipeIngredient (recipe_id, ingredient_id, measure_id, amount) VALUES (2, 4, 1, 1);
INSERT INTO RecipeIngredient (recipe_id, ingredient_id, measure_id, amount) VALUES (2, 10, 1, 1);
INSERT INTO RecipeIngredient (recipe_id, ingredient_id, measure_id, amount) VALUES (2, 11, 3, 1);

INSERT INTO RecipeIngredient (recipe_id, ingredient_id, measure_id, amount) VALUES (3, 2, 4, 2);
INSERT INTO RecipeIngredient (recipe_id, ingredient_id, measure_id, amount) VALUES (3, 3, 3, 2);
INSERT INTO RecipeIngredient (recipe_id, ingredient_id, measure_id, amount) VALUES (3, 4, 4, 1);












