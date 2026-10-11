-- 🍕 PIZZA TUB TRACKER 💜

local PizzaTub = {
    MinimumIncome = 100,
    Targets = {}
}

function PizzaTub:Add(name, income, isOG, mutation, traits)
    table.insert(self.Targets, {
        Name = name,
        Income = income,
        IsOG = isOG or false,
        Mutation = mutation or "None",
        Traits = traits or "None"
    })
end

function PizzaTub:GetMatches()
    local matches = {}

    for _, brainrot in ipairs(self.Targets) do
        if brainrot.IsOG or
           brainrot.Income >= self.MinimumIncome then
            table.insert(matches, brainrot)
        end
    end

    return matches
end

function PizzaTub:PrintMatches()
    print("🍕 ===== PIZZA TUB ===== 🍕")

    for _, b in ipairs(self:GetMatches()) do
        print("Name: " .. b.Name)
        print("Income: $" .. b.Income .. "M/s")
        print("OG: " .. tostring(b.IsOG))
        print("Mutation: " .. b.Mutation)
        print("Traits: " .. b.Traits)
        print("-----------------------")
    end
end

-- Example entries
PizzaTub:Add("Example OG", 10, true, "Rainbow", "None")
PizzaTub:Add("Example Brainrot", 150, false, "Gold", "Diamond Trait")

PizzaTub:PrintMatches()

return PizzaTub
